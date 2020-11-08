---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029736"
---
# <span data-ttu-id="d608f-101">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d608f-101">Get-AzureWebsite</span></span>

## <span data-ttu-id="d608f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d608f-102">SYNOPSIS</span></span>
<span data-ttu-id="d608f-103">Ottiene i siti Web di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="d608f-103">Gets Azure websites in the current subscription.</span></span>

## <span data-ttu-id="d608f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d608f-104">SYNTAX</span></span>

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d608f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d608f-105">DESCRIPTION</span></span>
<span data-ttu-id="d608f-106">Il cmdlet **Get-AzureWebsite** ottiene le informazioni sui siti Web di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="d608f-106">The **Get-AzureWebsite** cmdlet gets information about Azure websites in the current subscription.</span></span>

<span data-ttu-id="d608f-107">Per impostazione predefinita, **Get-AzureWebsite** ottiene tutti i siti Web di Azure nell'abbonamento corrente e restituisce un oggetto che fornisce informazioni di base sui siti.</span><span class="sxs-lookup"><span data-stu-id="d608f-107">By default, **Get-AzureWebsite** gets all Azure websites in the current subscription and returns an object that provides basic information about the sites.</span></span>
<span data-ttu-id="d608f-108">Quando si usa il parametro *Name* , **Get-AzureWebsite** restituisce un oggetto con informazioni estese, inclusi i dettagli della configurazione.</span><span class="sxs-lookup"><span data-stu-id="d608f-108">When you use the *Name* parameter, **Get-AzureWebsite** returns an object with extensive information, including configuration details.</span></span>

<span data-ttu-id="d608f-109">L'abbonamento corrente è l'abbonamento designato come "Current".</span><span class="sxs-lookup"><span data-stu-id="d608f-109">The current subscription is the subscription that is designated as "current."</span></span> <span data-ttu-id="d608f-110">Per trovare l'abbonamento corrente, usa il parametro *Current* del cmdlet [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) .</span><span class="sxs-lookup"><span data-stu-id="d608f-110">To find the current subscription, use the *Current* parameter of the [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) cmdlet.</span></span>
<span data-ttu-id="d608f-111">Per cambiare l'abbonamento corrente, usare il cmdlet [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) .</span><span class="sxs-lookup"><span data-stu-id="d608f-111">To change the current subscription, use the [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) cmdlet.</span></span>

<span data-ttu-id="d608f-112">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d608f-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d608f-113">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d608f-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="d608f-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d608f-114">EXAMPLES</span></span>

### <span data-ttu-id="d608f-115">Esempio 1: ottenere tutti i siti Web nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="d608f-115">Example 1: Get all websites in the subscription</span></span>
```
PS C:\> Get-AzureWebsite
```

<span data-ttu-id="d608f-116">Questo comando consente di ottenere tutti i siti Web di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="d608f-116">This command gets all Azure websites in the current subscription.</span></span>

### <span data-ttu-id="d608f-117">Esempio 2: ottenere un sito Web per nome</span><span class="sxs-lookup"><span data-stu-id="d608f-117">Example 2: Get a website by name</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

<span data-ttu-id="d608f-118">Questo comando consente di ottenere informazioni dettagliate sul sito Web di ContosoWeb Azure, incluse le informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="d608f-118">This command gets detailed information about the ContosoWeb Azure website, including configuration information.</span></span>
<span data-ttu-id="d608f-119">Quando usi il parametro *Name* , **Get-AzureWebsite** restituisce un oggetto **SiteWithConfig** con informazioni estese sul sito Web.</span><span class="sxs-lookup"><span data-stu-id="d608f-119">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object with extended information about the website.</span></span>

### <span data-ttu-id="d608f-120">Esempio 3: ottenere informazioni dettagliate su tutti i siti Web</span><span class="sxs-lookup"><span data-stu-id="d608f-120">Example 3: Get detailed information about all websites</span></span>
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

<span data-ttu-id="d608f-121">Questo comando consente di ottenere informazioni dettagliate su tutti i siti Web nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d608f-121">This command gets detailed information about all websites in the subscription.</span></span>
<span data-ttu-id="d608f-122">Usa un comando **Get-AzureWebsite** per ottenere tutti i siti Web e quindi usa il cmdlet **foreach-Object** per ottenere ogni sito Web per nome.</span><span class="sxs-lookup"><span data-stu-id="d608f-122">It uses a **Get-AzureWebsite** command to get all websites and then uses the **ForEach-Object** cmdlet to get each website by name.</span></span>

### <span data-ttu-id="d608f-123">Esempio 4: ottenere informazioni su uno slot di distribuzione</span><span class="sxs-lookup"><span data-stu-id="d608f-123">Example 4: Get information about a deployment slot</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

<span data-ttu-id="d608f-124">Questo comando ottiene lo slot di distribuzione della gestione temporanea del sito Web ContosoWeb.</span><span class="sxs-lookup"><span data-stu-id="d608f-124">This command gets the Staging deployment slot of the ContosoWeb website.</span></span>
<span data-ttu-id="d608f-125">Gli slot di distribuzione consentono di testare versioni diverse del sito Web di Azure senza rilasciarle al pubblico.</span><span class="sxs-lookup"><span data-stu-id="d608f-125">Deployment slots let you test different versions of your Azure website without releasing them to the public.</span></span>

### <span data-ttu-id="d608f-126">Esempio 5: ottenere istanze del sito Web</span><span class="sxs-lookup"><span data-stu-id="d608f-126">Example 5: Get website instances</span></span>
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

<span data-ttu-id="d608f-127">I comandi in questo esempio usano la proprietà instances di un sito Web di Azure per ottenere informazioni sulle istanze del sito Web attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="d608f-127">The commands in this example use the Instances property of an Azure website to get information about currently running website instances.</span></span>
<span data-ttu-id="d608f-128">La proprietà **instances** è stata aggiunta all'oggetto **SiteWithConfig** nella versione 0.8.3 del modulo Azure.</span><span class="sxs-lookup"><span data-stu-id="d608f-128">The **Instances** property was added to the **SiteWithConfig** object in version 0.8.3 of the Azure module.</span></span>

<span data-ttu-id="d608f-129">Il primo comando consente di ottenere gli ID di istanza di tutte le istanze attualmente in uso di un sito Web.</span><span class="sxs-lookup"><span data-stu-id="d608f-129">The first command gets the instance IDs of all currently running instances of a website.</span></span>
<span data-ttu-id="d608f-130">Il secondo comando consente di ottenere il numero di istanze in uso del sito Web.</span><span class="sxs-lookup"><span data-stu-id="d608f-130">The second command gets the number of running instances of the website.</span></span>
<span data-ttu-id="d608f-131">Puoi usare la proprietà **count** in qualsiasi matrice.</span><span class="sxs-lookup"><span data-stu-id="d608f-131">You can use the **Count** property on any array.</span></span>

## <span data-ttu-id="d608f-132">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d608f-132">PARAMETERS</span></span>

### <span data-ttu-id="d608f-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="d608f-133">-Name</span></span>
<span data-ttu-id="d608f-134">Ottiene informazioni dettagliate sulla configurazione del sito Web specificato.</span><span class="sxs-lookup"><span data-stu-id="d608f-134">Gets detailed configuration information about the specified website.</span></span>
<span data-ttu-id="d608f-135">Immettere il nome di un sito Web nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d608f-135">Enter the name of one website in the subscription.</span></span>
<span data-ttu-id="d608f-136">Per impostazione predefinita, **Get-AzureWebsite** ottiene tutti i siti Web nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="d608f-136">By default, **Get-AzureWebsite** gets all websites in the current subscription.</span></span>
<span data-ttu-id="d608f-137">Il valore *Name* non supporta i caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="d608f-137">The *Name* value does not support wildcard characters.</span></span>

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

### <span data-ttu-id="d608f-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="d608f-138">-Profile</span></span>
<span data-ttu-id="d608f-139">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d608f-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d608f-140">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d608f-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d608f-141">-Slot</span><span class="sxs-lookup"><span data-stu-id="d608f-141">-Slot</span></span>
<span data-ttu-id="d608f-142">Ottiene lo slot di distribuzione specificato del sito Web.</span><span class="sxs-lookup"><span data-stu-id="d608f-142">Gets the specified deployment slot of the website.</span></span>
<span data-ttu-id="d608f-143">Immettere il nome dello slot, ad esempio "Staging" o "Production".</span><span class="sxs-lookup"><span data-stu-id="d608f-143">Enter the slot name, such as "Staging" or "Production".</span></span>
<span data-ttu-id="d608f-144">Per altre informazioni sugli slot di distribuzione, vedere distribuzione a fasi nei siti Web di Microsoft Azure https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .</span><span class="sxs-lookup"><span data-stu-id="d608f-144">For more information about deployment slots, see Staged Deployment on Microsoft Azure Web Siteshttps://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/.</span></span>
<span data-ttu-id="d608f-145">Per aggiungere uno slot di distribuzione a un sito Web Azure esistente, usare il cmdlet Set-AzureWebsite.</span><span class="sxs-lookup"><span data-stu-id="d608f-145">To add a deployment slot to an existing Azure website, use the Set-AzureWebsite cmdlet.</span></span>

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

### <span data-ttu-id="d608f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d608f-146">CommonParameters</span></span>
<span data-ttu-id="d608f-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d608f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d608f-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d608f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d608f-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d608f-149">INPUTS</span></span>

### <span data-ttu-id="d608f-150">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d608f-150">None</span></span>
<span data-ttu-id="d608f-151">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="d608f-151">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="d608f-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d608f-152">OUTPUTS</span></span>

### <span data-ttu-id="d608f-153">Microsoft. WindowsAzure. Commands. Utilities. Web. Services. webentities. site</span><span class="sxs-lookup"><span data-stu-id="d608f-153">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.Site</span></span>
<span data-ttu-id="d608f-154">Per impostazione predefinita, **Get-AzureWebsite** restituisce una matrice di oggetti **sito** .</span><span class="sxs-lookup"><span data-stu-id="d608f-154">By default, **Get-AzureWebsite** returns an array of **Site** objects.</span></span>

### <span data-ttu-id="d608f-155">Microsoft. WindowsAzure. Commands. Utilities. Web. Services. webentities. SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="d608f-155">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.SiteWithConfig</span></span>
<span data-ttu-id="d608f-156">Quando usi il parametro *Name* , **Get-AzureWebsite** restituisce un oggetto **SiteWithConfig** .</span><span class="sxs-lookup"><span data-stu-id="d608f-156">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object.</span></span>

## <span data-ttu-id="d608f-157">Note</span><span class="sxs-lookup"><span data-stu-id="d608f-157">NOTES</span></span>

## <span data-ttu-id="d608f-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d608f-158">RELATED LINKS</span></span>

[<span data-ttu-id="d608f-159">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d608f-159">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="d608f-160">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d608f-160">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="d608f-161">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d608f-161">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="d608f-162">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d608f-162">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="d608f-163">Mostra-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d608f-163">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


