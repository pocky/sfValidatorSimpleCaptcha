# A propos #

Ce validateur à pour but de proposer un captcha très simple basé sur une simple addition.

## Utilisation ##
__En supposant que le champ de votre formulaire s'appelle captcha__

    <?php
      
      class ContactForm extends BaseForm
      {
        public function configure()
        {
          [...]
          
          $this->setValidators(array(
            'captcha'	  => new sfValidatorSimpleCaptcha(array(
          	  'required'     => true,
          	  'first_number' => 3,
          	  'last_number'  => 4,
          	), array(
          		'required'     => 'Captcha is required',
          	)),
          ));
        }
      }