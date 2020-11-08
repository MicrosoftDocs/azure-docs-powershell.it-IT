---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023828"
---
# <span data-ttu-id="676e3-101">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="676e3-101">Remove-AzureAccount</span></span>

## <span data-ttu-id="676e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="676e3-102">SYNOPSIS</span></span>
<span data-ttu-id="676e3-103">Elimina un account Azure da Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="676e3-103">Deletes an Azure account from Windows PowerShell.</span></span>

## <span data-ttu-id="676e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="676e3-104">SYNTAX</span></span>

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="676e3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="676e3-105">DESCRIPTION</span></span>
<span data-ttu-id="676e3-106">Il cmdlet **Remove-AzureAccount** Elimina un account Azure e i relativi abbonamenti dal file di dati dell'abbonamento nel profilo utente mobile.</span><span class="sxs-lookup"><span data-stu-id="676e3-106">The **Remove-AzureAccount** cmdlet deletes an Azure account and its subscriptions from the subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="676e3-107">Non elimina l'account da Microsoft Azure o modifica l'account effettivo in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="676e3-107">It does not delete the account from Microsoft Azure, or change the actual account in any way.</span></span>

<span data-ttu-id="676e3-108">L'uso di questo cmdlet è molto simile alla disconnessione dall'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="676e3-108">Using this cmdlet is a lot like logging out of your Azure account.</span></span>
<span data-ttu-id="676e3-109">Se si vuole accedere di nuovo all'account, usare il **componente aggiuntivo AzureAccount** o **Import-AzurePublishSettingsFile** per aggiungere di nuovo l'account a Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="676e3-109">And, if you want to log into the account again, use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** to add the account to Windows PowerShell again.</span></span>

<span data-ttu-id="676e3-110">Puoi anche usare il cmdlet **Remove-AzureAccount** per cambiare il modo in cui i cmdlet di PowerShell di Azure si iscrivono all'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="676e3-110">You can also use **Remove-AzureAccount** cmdlet to change the way the Azure PowerShell cmdlets sign into your Azure account.</span></span>
<span data-ttu-id="676e3-111">Se l'account include sia un certificato di gestione da **Import-AzurePublishSettingsFile** che un token di accesso da **Add-AzureAccount** , i cmdlet di PowerShell di Azure usano solo il token di accesso. ignorano il certificato di gestione.</span><span class="sxs-lookup"><span data-stu-id="676e3-111">If your account has both a management certificate from **Import-AzurePublishSettingsFile** and an access token from **Add-AzureAccount** , the Azure PowerShell cmdlets use only the access token; they ignore the management certificate.</span></span>
<span data-ttu-id="676e3-112">Per usare il certificato di gestione, eseguire **Remove-AzureAccount**.</span><span class="sxs-lookup"><span data-stu-id="676e3-112">To use the management certificate, run **Remove-AzureAccount**.</span></span>
<span data-ttu-id="676e3-113">Quando **Remove-AzureAccount** trova sia un certificato di gestione che un token di accesso, Elimina solo il token di accesso anziché eliminare l'account.</span><span class="sxs-lookup"><span data-stu-id="676e3-113">When **Remove-AzureAccount** finds both a management certificate and an access token, it deletes only the access token, instead of deleting the account.</span></span>
<span data-ttu-id="676e3-114">Il certificato di gestione è ancora presente, quindi l'account è ancora disponibile per Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="676e3-114">The management certificate is still there, so account is still available to Windows PowerShell.</span></span>

<span data-ttu-id="676e3-115">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="676e3-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="676e3-116">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="676e3-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="676e3-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="676e3-117">EXAMPLES</span></span>

### <span data-ttu-id="676e3-118">Esempio 1: rimuovere un account</span><span class="sxs-lookup"><span data-stu-id="676e3-118">Example 1: Remove an account</span></span>
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

<span data-ttu-id="676e3-119">Questo comando rimuove admin@contoso.com dal file di dati dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="676e3-119">This command removes the admin@contoso.com from your subscription data file.</span></span>
<span data-ttu-id="676e3-120">Al termine del comando, l'account non è più disponibile per Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="676e3-120">When the command completes, the account is no longer available to Windows PowerShell.</span></span>

## <span data-ttu-id="676e3-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="676e3-121">PARAMETERS</span></span>

### <span data-ttu-id="676e3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="676e3-122">-Force</span></span>
<span data-ttu-id="676e3-123">Elimina la richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="676e3-123">Suppresses the confirmation prompt.</span></span>
<span data-ttu-id="676e3-124">Per impostazione predefinita, **Remove-AzureAccount** richiede prima di rimuovere l'account da Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="676e3-124">By default, **Remove-AzureAccount** prompts you before removing the account from Windows PowerShell.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676e3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="676e3-125">-Name</span></span>
<span data-ttu-id="676e3-126">Specifica il nome dell'account da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="676e3-126">Specifies the name of the account to remove.</span></span>
<span data-ttu-id="676e3-127">Il valore del parametro fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="676e3-127">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="676e3-128">I caratteri jolly non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="676e3-128">Wildcard characters are not supported.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="676e3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="676e3-129">-PassThru</span></span>
<span data-ttu-id="676e3-130">Restituisce $True se il comando riesce e $False se non riesce.</span><span class="sxs-lookup"><span data-stu-id="676e3-130">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="676e3-131">Per impostazione predefinita, questo cmdlet non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="676e3-131">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676e3-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="676e3-132">-Profile</span></span>
<span data-ttu-id="676e3-133">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="676e3-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="676e3-134">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="676e3-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676e3-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="676e3-135">-Confirm</span></span>
<span data-ttu-id="676e3-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="676e3-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676e3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="676e3-137">-WhatIf</span></span>
<span data-ttu-id="676e3-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="676e3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="676e3-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="676e3-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676e3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="676e3-140">CommonParameters</span></span>
<span data-ttu-id="676e3-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="676e3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="676e3-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="676e3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="676e3-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="676e3-143">INPUTS</span></span>

### <span data-ttu-id="676e3-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="676e3-144">None</span></span>
<span data-ttu-id="676e3-145">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="676e3-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="676e3-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="676e3-146">OUTPUTS</span></span>

### <span data-ttu-id="676e3-147">None o System. Boolean</span><span class="sxs-lookup"><span data-stu-id="676e3-147">None or System.Boolean</span></span>
<span data-ttu-id="676e3-148">Se si usa il parametro *PassThru* , questo cmdlet restituisce un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="676e3-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="676e3-149">In caso contrario, non restituirà alcun output.</span><span class="sxs-lookup"><span data-stu-id="676e3-149">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="676e3-150">Note</span><span class="sxs-lookup"><span data-stu-id="676e3-150">NOTES</span></span>

## <span data-ttu-id="676e3-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="676e3-151">RELATED LINKS</span></span>

[<span data-ttu-id="676e3-152">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="676e3-152">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="676e3-153">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="676e3-153">Get-AzureAccount</span></span>](./Get-AzureAccount.md)


