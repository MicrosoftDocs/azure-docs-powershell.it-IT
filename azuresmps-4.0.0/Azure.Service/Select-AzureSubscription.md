---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 7A45DCAD-88DC-40F0-BBF7-0F531A571CA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b941691366c3af821e3a4cdaa7b07c5e958e16
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023403"
---
# <span data-ttu-id="3ec80-101">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="3ec80-101">Select-AzureSubscription</span></span>

## <span data-ttu-id="3ec80-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ec80-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec80-103">Modifica le sottoscrizioni di Azure correnti e predefinite.</span><span class="sxs-lookup"><span data-stu-id="3ec80-103">Changes the current and default Azure subscriptions.</span></span>

## <span data-ttu-id="3ec80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ec80-104">SYNTAX</span></span>

### <span data-ttu-id="3ec80-105">SelectSubscriptionByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3ec80-105">SelectSubscriptionByNameParameterSet (Default)</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3ec80-106">SelectDefaultSubscriptionByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ec80-106">SelectDefaultSubscriptionByNameParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3ec80-107">SelectSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ec80-107">SelectSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3ec80-108">SelectDefaultSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ec80-108">SelectDefaultSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3ec80-109">NoCurrentSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ec80-109">NoCurrentSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoCurrent] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ec80-110">NoDefaultSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ec80-110">NoDefaultSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoDefault] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ec80-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ec80-111">DESCRIPTION</span></span>
<span data-ttu-id="3ec80-112">Il cmdlet **Select-AzureSubscription** imposta e cancella gli abbonamenti Azure correnti e predefiniti.</span><span class="sxs-lookup"><span data-stu-id="3ec80-112">The **Select-AzureSubscription** cmdlet sets and clears the current and default Azure subscriptions.</span></span>

<span data-ttu-id="3ec80-113">"Abbonamento corrente" è l'abbonamento usato per impostazione predefinita nella sessione corrente di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3ec80-113">The "current subscription" is the subscription that is used by default in the current Windows PowerShell session.</span></span>
<span data-ttu-id="3ec80-114">L'"abbonamento predefinito" viene usato per impostazione predefinita in tutte le sessioni di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3ec80-114">The "default subscription" is used by default in all Windows PowerShell sessions.</span></span>
<span data-ttu-id="3ec80-115">L'etichetta "abbonamento corrente" consente di specificare un abbonamento diverso da usare per impostazione predefinita per la sessione corrente senza modificare l'"abbonamento predefinito" per tutte le altre sessioni.</span><span class="sxs-lookup"><span data-stu-id="3ec80-115">The "current subscription" label lets you specify a different subscription to be used by default for the current session without changing the "default subscription" for all other sessions.</span></span>

<span data-ttu-id="3ec80-116">La denominazione di sottoscrizione "predefinita" viene salvata nel file di dati dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3ec80-116">The "default" subscription designation is saved in your subscription data file.</span></span>
<span data-ttu-id="3ec80-117">L'indicazione "Current" specifica della sessione non viene salvata.</span><span class="sxs-lookup"><span data-stu-id="3ec80-117">The session-specific "current" designation is not saved.</span></span>

<span data-ttu-id="3ec80-118">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec80-118">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3ec80-119">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3ec80-119">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="3ec80-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ec80-120">EXAMPLES</span></span>

### <span data-ttu-id="3ec80-121">Esempio 1: impostare l'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="3ec80-121">Example 1: Set the current subscription</span></span>
```
C:\PS> Select-AzureSubscription -Current -SubscriptionName ContosoEngineering
```

<span data-ttu-id="3ec80-122">Questo comando rende "ContosoEngineering" l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="3ec80-122">This command makes "ContosoEngineering" the current subscription.</span></span>

### <span data-ttu-id="3ec80-123">Esempio 2: impostare l'abbonamento predefinito</span><span class="sxs-lookup"><span data-stu-id="3ec80-123">Example 2: Set the default subscription</span></span>
```
C:\PS> Select-AzureSubscription -Default -SubscriptionName ContosoFinance -SubscriptionDataFile "C:\subs\MySubscriptions.xml"
```

<span data-ttu-id="3ec80-124">Questo comando modifica la sottoscrizione predefinita in "ContosoFinance".</span><span class="sxs-lookup"><span data-stu-id="3ec80-124">This command changes the default subscription to "ContosoFinance."</span></span> <span data-ttu-id="3ec80-125">Salva l'impostazione nel file di dati dell'abbonamento Subscriptions.xml anziché nel file di dati dell'abbonamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="3ec80-125">It saves the setting in the Subscriptions.xml subscription data file, instead of the default subscription data file.</span></span>

## <span data-ttu-id="3ec80-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ec80-126">PARAMETERS</span></span>

### <span data-ttu-id="3ec80-127">-Account</span><span class="sxs-lookup"><span data-stu-id="3ec80-127">-Account</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ec80-128">-Current</span><span class="sxs-lookup"><span data-stu-id="3ec80-128">-Current</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectSubscriptionByIdParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec80-129">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="3ec80-129">-Default</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectDefaultSubscriptionByNameParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec80-130">-Nocurrent</span><span class="sxs-lookup"><span data-stu-id="3ec80-130">-NoCurrent</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoCurrentSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec80-131">-NODEFAULT</span><span class="sxs-lookup"><span data-stu-id="3ec80-131">-NoDefault</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoDefaultSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec80-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ec80-132">-PassThru</span></span>
<span data-ttu-id="3ec80-133">Restituisce $True se il comando riesce e $False se non riesce.</span><span class="sxs-lookup"><span data-stu-id="3ec80-133">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="3ec80-134">Per impostazione predefinita, questo cmdlet non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="3ec80-134">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="3ec80-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="3ec80-135">-Profile</span></span>
<span data-ttu-id="3ec80-136">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ec80-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3ec80-137">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3ec80-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3ec80-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ec80-138">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByIdParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ec80-139">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="3ec80-139">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectDefaultSubscriptionByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ec80-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec80-140">CommonParameters</span></span>
<span data-ttu-id="3ec80-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ec80-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec80-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ec80-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec80-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ec80-143">INPUTS</span></span>

### <span data-ttu-id="3ec80-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3ec80-144">None</span></span>
<span data-ttu-id="3ec80-145">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="3ec80-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="3ec80-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ec80-146">OUTPUTS</span></span>

### <span data-ttu-id="3ec80-147">None o System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ec80-147">None or System.Boolean</span></span>
<span data-ttu-id="3ec80-148">Se si usa il parametro *PassThru* , questo cmdlet restituisce un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="3ec80-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="3ec80-149">Per impostazione predefinita, non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3ec80-149">By default, it does not generate any output.</span></span>

## <span data-ttu-id="3ec80-150">Note</span><span class="sxs-lookup"><span data-stu-id="3ec80-150">NOTES</span></span>

## <span data-ttu-id="3ec80-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ec80-151">RELATED LINKS</span></span>

[<span data-ttu-id="3ec80-152">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="3ec80-152">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="3ec80-153">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="3ec80-153">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="3ec80-154">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="3ec80-154">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


