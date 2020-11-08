---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: ABC303ED-8712-4958-B871-E95357012277
online version: ''
schema: 2.0.0
ms.openlocfilehash: 706c1dee2bc4bb21a8cf116d15bfa3e53daeed99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029557"
---
# <span data-ttu-id="0616f-101">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="0616f-101">Remove-AzureSubscription</span></span>

## <span data-ttu-id="0616f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0616f-102">SYNOPSIS</span></span>
<span data-ttu-id="0616f-103">Elimina un abbonamento a Azure da Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0616f-103">Deletes an Azure subscription from Windows PowerShell.</span></span>

## <span data-ttu-id="0616f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0616f-104">SYNTAX</span></span>

### <span data-ttu-id="0616f-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0616f-105">Name (Default)</span></span>
```
Remove-AzureSubscription -SubscriptionName <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0616f-106">ID</span><span class="sxs-lookup"><span data-stu-id="0616f-106">Id</span></span>
```
Remove-AzureSubscription -SubscriptionId <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0616f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0616f-107">DESCRIPTION</span></span>
<span data-ttu-id="0616f-108">Il cmdlet **Remove-AzureSubscription** Elimina un abbonamento Azure dal file di dati dell'abbonamento in modo che Windows PowerShell non riesca a trovarlo.</span><span class="sxs-lookup"><span data-stu-id="0616f-108">The **Remove-AzureSubscription** cmdlet deletes an Azure subscription from your subscription data file so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="0616f-109">Questo cmdlet non elimina l'abbonamento da Microsoft Azure o modifica in alcun modo l'abbonamento effettivo.</span><span class="sxs-lookup"><span data-stu-id="0616f-109">This cmdlet does not delete the subscription from Microsoft Azure, or change the actual subscription in any way.</span></span>

<span data-ttu-id="0616f-110">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0616f-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0616f-111">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0616f-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="0616f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0616f-112">EXAMPLES</span></span>

### <span data-ttu-id="0616f-113">Esempio 1: eliminare un abbonamento</span><span class="sxs-lookup"><span data-stu-id="0616f-113">Example 1: Delete a subscription</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test

Confirm
Are you sure you want to perform this action?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="0616f-114">Questo comando Elimina l'abbonamento "test" dal file di dati dell'abbonamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="0616f-114">This command deletes the "Test" subscription from the default subscription data file.</span></span>

### <span data-ttu-id="0616f-115">Esempio 2: eliminare da un file di dati di un abbonamento alternativo</span><span class="sxs-lookup"><span data-stu-id="0616f-115">Example 2: Delete from an alternate subscription data file</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test -SubscriptionDataFile C:\Subs\MySubscriptions.xml -Force
```

<span data-ttu-id="0616f-116">Questo comando Elimina la sottoscrizione di test dal file di dati dell'abbonamento MySubscriptions.xml.</span><span class="sxs-lookup"><span data-stu-id="0616f-116">This command deletes the Test subscription from the MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="0616f-117">Il comando usa il parametro *Force* per eliminare la richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="0616f-117">The command uses the *Force* parameter to suppress the confirmation prompt.</span></span>

### <span data-ttu-id="0616f-118">Esempio 3: eliminare un abbonamento in uno script</span><span class="sxs-lookup"><span data-stu-id="0616f-118">Example 3: Delete a subscription in a script</span></span>
```
C:\PS> ...if (Remove-AzureSubscription -SubscriptionName Test -PassThru) {...}
```

<span data-ttu-id="0616f-119">Questo comando usa il comando **Remove-AzureSubscription** in un'istruzione **if** .</span><span class="sxs-lookup"><span data-stu-id="0616f-119">This command uses the **Remove-AzureSubscription** command in an **If** statement.</span></span>
<span data-ttu-id="0616f-120">Usa il parametro *PassThru* , che restituisce un valore booleano, per determinare se il blocco di script nell'istruzione **if** viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0616f-120">It uses the *PassThru* parameter, which returns a Boolean value, to determine whether the script block in the **If** statement is executed.</span></span>

## <span data-ttu-id="0616f-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0616f-121">PARAMETERS</span></span>

### <span data-ttu-id="0616f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0616f-122">-Force</span></span>
<span data-ttu-id="0616f-123">Elimina la richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="0616f-123">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="0616f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0616f-124">-PassThru</span></span>
<span data-ttu-id="0616f-125">Restituisce $True se il comando riesce e $False se non riesce.</span><span class="sxs-lookup"><span data-stu-id="0616f-125">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="0616f-126">Per impostazione predefinita, questo cmdlet non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="0616f-126">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="0616f-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="0616f-127">-Profile</span></span>
<span data-ttu-id="0616f-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0616f-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0616f-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0616f-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0616f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0616f-130">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Id
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0616f-131">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="0616f-131">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: Name
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0616f-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0616f-132">-Confirm</span></span>
<span data-ttu-id="0616f-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0616f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0616f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0616f-134">-WhatIf</span></span>
<span data-ttu-id="0616f-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0616f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0616f-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0616f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0616f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0616f-137">CommonParameters</span></span>
<span data-ttu-id="0616f-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0616f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0616f-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0616f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0616f-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0616f-140">INPUTS</span></span>

### <span data-ttu-id="0616f-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0616f-141">None</span></span>
<span data-ttu-id="0616f-142">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="0616f-142">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="0616f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0616f-143">OUTPUTS</span></span>

### <span data-ttu-id="0616f-144">None o System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0616f-144">None or System.Boolean</span></span>
<span data-ttu-id="0616f-145">Se si usa il parametro *PassThru* , questo cmdlet restituisce un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="0616f-145">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="0616f-146">In caso contrario, non restituirà alcun output.</span><span class="sxs-lookup"><span data-stu-id="0616f-146">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="0616f-147">Note</span><span class="sxs-lookup"><span data-stu-id="0616f-147">NOTES</span></span>

## <span data-ttu-id="0616f-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0616f-148">RELATED LINKS</span></span>

[<span data-ttu-id="0616f-149">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="0616f-149">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="0616f-150">Selezionare-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="0616f-150">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)

[<span data-ttu-id="0616f-151">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="0616f-151">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


