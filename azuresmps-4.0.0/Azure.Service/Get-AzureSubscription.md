---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023495"
---
# <span data-ttu-id="05ea2-101">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="05ea2-101">Get-AzureSubscription</span></span>

## <span data-ttu-id="05ea2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="05ea2-103">Ottiene abbonamenti Azure in account Azure.</span><span class="sxs-lookup"><span data-stu-id="05ea2-103">Gets  Azure subscriptions in Azure account.</span></span>

## <span data-ttu-id="05ea2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05ea2-104">SYNTAX</span></span>

### <span data-ttu-id="05ea2-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="05ea2-105">ByName (Default)</span></span>
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="05ea2-106">ById</span><span class="sxs-lookup"><span data-stu-id="05ea2-106">ById</span></span>
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="05ea2-107">Predefinita</span><span class="sxs-lookup"><span data-stu-id="05ea2-107">Default</span></span>
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="05ea2-108">Corrente</span><span class="sxs-lookup"><span data-stu-id="05ea2-108">Current</span></span>
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="05ea2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05ea2-109">DESCRIPTION</span></span>
<span data-ttu-id="05ea2-110">Il cmdlet **Get-AzureSubscription** ottiene le sottoscrizioni nell'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="05ea2-110">The **Get-AzureSubscription** cmdlet gets the subscriptions in your Azure account.</span></span>
<span data-ttu-id="05ea2-111">Puoi usare questo cmdlet per ottenere informazioni sull'abbonamento e per reindirizzare l'abbonamento ad altri cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05ea2-111">You can use this cmdlet to get information about the subscription and to pipe the subscription to other cmdlets.</span></span>

<span data-ttu-id="05ea2-112">**Get-AzureSubscription** richiede l'accesso agli account di Azure.</span><span class="sxs-lookup"><span data-stu-id="05ea2-112">**Get-AzureSubscription** requires access to your Azure accounts.</span></span>
<span data-ttu-id="05ea2-113">Prima di eseguire **Get-AzureSubscription** , è necessario eseguire il cmdlet **Add-AzureAccount** o i cmdlet che scaricano e installano un file di impostazioni di pubblicazione ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span><span class="sxs-lookup"><span data-stu-id="05ea2-113">Before you run **Get-AzureSubscription** , you must run the **Add-AzureAccount** cmdlet or the cmdlets that download and install a publish settings file ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span></span>

<span data-ttu-id="05ea2-114">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="05ea2-114">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="05ea2-115">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="05ea2-115">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="05ea2-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05ea2-116">EXAMPLES</span></span>

### <span data-ttu-id="05ea2-117">Esempio 1: ottenere tutte le sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="05ea2-117">Example 1: Get all subscriptions</span></span>
```
C:\PS>Get-AzureSubscription
```

<span data-ttu-id="05ea2-118">Questo comando consente di ottenere tutte le sottoscrizioni nell'account.</span><span class="sxs-lookup"><span data-stu-id="05ea2-118">This command gets all subscriptions in the account.</span></span>

### <span data-ttu-id="05ea2-119">Esempio 2: ottenere un abbonamento per nome</span><span class="sxs-lookup"><span data-stu-id="05ea2-119">Example 2: Get a subscription by name</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

<span data-ttu-id="05ea2-120">Questo comando ottiene solo l'abbonamento "MyProdSubsciption".</span><span class="sxs-lookup"><span data-stu-id="05ea2-120">This command gets only the "MyProdSubsciption" subscription.</span></span>

### <span data-ttu-id="05ea2-121">Esempio 3: ottenere l'abbonamento predefinito</span><span class="sxs-lookup"><span data-stu-id="05ea2-121">Example 3: Get the default subscription</span></span>
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

<span data-ttu-id="05ea2-122">Questo comando ottiene solo il nome dell'abbonamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="05ea2-122">This command gets only the name of the default subscription.</span></span>
<span data-ttu-id="05ea2-123">Il comando ottiene prima di tutto l'abbonamento e quindi usa il metodo dot per ottenere la proprietà **subscriptionname** dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="05ea2-123">The command first gets the subscription and then uses the dot method to get the **SubscriptionName** property of the subscription.</span></span>

### <span data-ttu-id="05ea2-124">Esempio 4: ottenere le proprietà di sottoscrizione selezionate</span><span class="sxs-lookup"><span data-stu-id="05ea2-124">Example 4: Get selected subscription properties</span></span>
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

<span data-ttu-id="05ea2-125">Questo comando restituisce un elenco con il nome e il certificato della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="05ea2-125">This command returns a list with the name and certificate of the current subscription.</span></span>
<span data-ttu-id="05ea2-126">Usa un comando **Get-AzureSubscription** per ottenere l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="05ea2-126">It uses a **Get-AzureSubscription** command to get the current subscription.</span></span>
<span data-ttu-id="05ea2-127">Quindi convoglia l'abbonamento a un comando **Format-List** che visualizza le proprietà selezionate in un elenco.</span><span class="sxs-lookup"><span data-stu-id="05ea2-127">Then it pipes the subscription to a **Format-List** command that displays the selected properties in a list.</span></span>

### <span data-ttu-id="05ea2-128">Esempio 5: usare un file di dati alternativo per l'abbonamento</span><span class="sxs-lookup"><span data-stu-id="05ea2-128">Example 5: Use an alternate subscription data file</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

<span data-ttu-id="05ea2-129">Questo comando ottiene gli abbonamenti dal file di dati dell'abbonamento C:\Temp\MySubscriptions.xml.</span><span class="sxs-lookup"><span data-stu-id="05ea2-129">This command gets subscriptions from  the C:\Temp\MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="05ea2-130">Usa il parametro **SubscriptionDataFile** se hai specificato un file di dati di sottoscrizione alternativo quando hai eseguito i cmdlet **Add-AzureAccount** o **Import-PublishSettingsFile** .</span><span class="sxs-lookup"><span data-stu-id="05ea2-130">Use the **SubscriptionDataFile** parameter if you specified an alternate subscription data file when you ran the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="05ea2-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05ea2-131">PARAMETERS</span></span>

### <span data-ttu-id="05ea2-132">-Current</span><span class="sxs-lookup"><span data-stu-id="05ea2-132">-Current</span></span>
<span data-ttu-id="05ea2-133">Ottiene solo l'abbonamento corrente, ovvero l'abbonamento designato come "corrente".</span><span class="sxs-lookup"><span data-stu-id="05ea2-133">Gets only the current subscription, that is, the subscription designated as "current."</span></span> <span data-ttu-id="05ea2-134">Per impostazione predefinita, **Get-AzureSubscription** ottiene tutte le sottoscrizioni degli account di Azure.</span><span class="sxs-lookup"><span data-stu-id="05ea2-134">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="05ea2-135">Per designare un abbonamento come "corrente", usa il parametro **Current** del cmdlet **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="05ea2-135">To designate a subscription as "current," use the **Current** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ea2-136">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="05ea2-136">-Default</span></span>
<span data-ttu-id="05ea2-137">Ottiene solo l'abbonamento predefinito, ovvero l'abbonamento designato come "predefinito".</span><span class="sxs-lookup"><span data-stu-id="05ea2-137">Gets only the default subscription, that is, the subscription designated as "default."</span></span> <span data-ttu-id="05ea2-138">Per impostazione predefinita, **Get-AzureSubscription** ottiene tutte le sottoscrizioni degli account di Azure.</span><span class="sxs-lookup"><span data-stu-id="05ea2-138">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="05ea2-139">Per designare un abbonamento come "predefinito", usare il parametro **predefinito** del cmdlet **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="05ea2-139">To designate a subscription as "default," use the **Default** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ea2-140">-ExtendedDetails</span><span class="sxs-lookup"><span data-stu-id="05ea2-140">-ExtendedDetails</span></span>
<span data-ttu-id="05ea2-141">Restituisce le informazioni sulle quote per l'abbonamento, oltre alle impostazioni standard.</span><span class="sxs-lookup"><span data-stu-id="05ea2-141">Returns quota information for the subscription, in addition to the standard settings.</span></span>

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

### <span data-ttu-id="05ea2-142">-Profile</span><span class="sxs-lookup"><span data-stu-id="05ea2-142">-Profile</span></span>
<span data-ttu-id="05ea2-143">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05ea2-143">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="05ea2-144">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="05ea2-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05ea2-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05ea2-145">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05ea2-146">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="05ea2-146">-SubscriptionName</span></span>
<span data-ttu-id="05ea2-147">Ottiene solo l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="05ea2-147">Gets only the specified subscription.</span></span>
<span data-ttu-id="05ea2-148">Immettere il nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="05ea2-148">Enter the subscription name.</span></span>
<span data-ttu-id="05ea2-149">Il valore fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="05ea2-149">The value is case-sensitive.</span></span>
<span data-ttu-id="05ea2-150">I caratteri jolly non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="05ea2-150">Wildcard characters are not supported.</span></span>
<span data-ttu-id="05ea2-151">Per impostazione predefinita, **Get-AzureSubscription** ottiene tutte le sottoscrizioni degli account di Azure.</span><span class="sxs-lookup"><span data-stu-id="05ea2-151">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05ea2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ea2-152">CommonParameters</span></span>
<span data-ttu-id="05ea2-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05ea2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ea2-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05ea2-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ea2-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05ea2-155">INPUTS</span></span>

### <span data-ttu-id="05ea2-156">Nessuno</span><span class="sxs-lookup"><span data-stu-id="05ea2-156">None</span></span>
<span data-ttu-id="05ea2-157">È possibile reindirizzare l'input alla proprietà **subscriptionname** per nome, ma non per valore.</span><span class="sxs-lookup"><span data-stu-id="05ea2-157">You can pipe input to the **SubscriptionName** property by name, but not by value.</span></span>

## <span data-ttu-id="05ea2-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05ea2-158">OUTPUTS</span></span>

### <span data-ttu-id="05ea2-159">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="05ea2-159">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureSubscription</span></span>

## <span data-ttu-id="05ea2-160">Note</span><span class="sxs-lookup"><span data-stu-id="05ea2-160">NOTES</span></span>
* <span data-ttu-id="05ea2-161">Get-AzureSubscription ottiene i dati dal file di dati dell'abbonamento creato dai cmdlet **Add-AzureAccount** e **Import-PublishSettingsFile** .</span><span class="sxs-lookup"><span data-stu-id="05ea2-161">Get-AzureSubscription gets data from the subscription data file that the **Add-AzureAccount** and **Import-PublishSettingsFile** cmdlets create.</span></span>

## <span data-ttu-id="05ea2-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05ea2-162">RELATED LINKS</span></span>

[<span data-ttu-id="05ea2-163">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="05ea2-163">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="05ea2-164">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="05ea2-164">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="05ea2-165">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="05ea2-165">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="05ea2-166">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="05ea2-166">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="05ea2-167">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="05ea2-167">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


