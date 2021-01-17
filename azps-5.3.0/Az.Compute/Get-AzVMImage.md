---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 350e03d6e238eb0cf1aa6b27da6b9a321603a664
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488476"
---
# <span data-ttu-id="4430d-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4430d-101">Get-AzVMImage</span></span>

## <span data-ttu-id="4430d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4430d-102">SYNOPSIS</span></span>
<span data-ttu-id="4430d-103">Ottiene tutte le versioni di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="4430d-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="4430d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4430d-104">SYNTAX</span></span>

### <span data-ttu-id="4430d-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="4430d-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4430d-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="4430d-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4430d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4430d-107">DESCRIPTION</span></span>
<span data-ttu-id="4430d-108">Il cmdlet **Get-AzVMImage** ottiene tutte le versioni di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="4430d-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="4430d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4430d-109">EXAMPLES</span></span>

### <span data-ttu-id="4430d-110">Esempio 1: ottenere oggetti VMImage</span><span class="sxs-lookup"><span data-stu-id="4430d-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="4430d-111">Questo comando consente di ottenere tutte le versioni di VMImage che corrispondono ai valori specificati.</span><span class="sxs-lookup"><span data-stu-id="4430d-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="4430d-112">Esempio 2: ottenere l'oggetto VMImage</span><span class="sxs-lookup"><span data-stu-id="4430d-112">Example 2: Get VMImage object</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.20180315

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/centralus/
                   Publishers/MicrosoftWindowsServer/ArtifactTypes/VMImage/Offers/windowsserver/Skus/2012-R2-Datacenter
                   /Versions/4.127.20180315
Location         : centralus
PublisherName    : MicrosoftWindowsServer
Offer            : windowsserver
Skus             : 2012-R2-Datacenter
Version          : 4.127.20180315
FilterExpression :
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="4430d-113">Questo comando ottiene una versione specifica di VMImage che corrisponde ai valori specificati.</span><span class="sxs-lookup"><span data-stu-id="4430d-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="4430d-114">Esempio 3: ottenere oggetti VMImage</span><span class="sxs-lookup"><span data-stu-id="4430d-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="4430d-115">Questo comando consente di ottenere tutte le versioni di VMImage che corrispondono ai valori specificati con il filtro sulla versione.</span><span class="sxs-lookup"><span data-stu-id="4430d-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="4430d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4430d-116">PARAMETERS</span></span>

### <span data-ttu-id="4430d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4430d-117">-DefaultProfile</span></span>
<span data-ttu-id="4430d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4430d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4430d-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4430d-119">-Location</span></span>
<span data-ttu-id="4430d-120">Specifica la posizione di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="4430d-120">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4430d-121">-Offerta</span><span class="sxs-lookup"><span data-stu-id="4430d-121">-Offer</span></span>
<span data-ttu-id="4430d-122">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="4430d-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="4430d-123">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="4430d-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4430d-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="4430d-124">-OrderBy</span></span>
<span data-ttu-id="4430d-125">Specifica l'ordine dei risultati restituiti.</span><span class="sxs-lookup"><span data-stu-id="4430d-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="4430d-126">Formattato come query OData.</span><span class="sxs-lookup"><span data-stu-id="4430d-126">Formatted as an OData query.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4430d-127">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4430d-127">-PublisherName</span></span>
<span data-ttu-id="4430d-128">Specifica l'autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="4430d-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="4430d-129">Per ottenere un autore di immagini, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="4430d-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4430d-130">-SKU</span><span class="sxs-lookup"><span data-stu-id="4430d-130">-Skus</span></span>
<span data-ttu-id="4430d-131">Specifica una SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="4430d-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="4430d-132">Per ottenere un SKU, usare il cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="4430d-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4430d-133">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="4430d-133">-Top</span></span>
<span data-ttu-id="4430d-134">Specifica il numero massimo di immagini della macchina virtuale restituite.</span><span class="sxs-lookup"><span data-stu-id="4430d-134">Specifies the maximum number of virtual machine images returned.</span></span> 

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4430d-135">-Versione</span><span class="sxs-lookup"><span data-stu-id="4430d-135">-Version</span></span>
<span data-ttu-id="4430d-136">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="4430d-136">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4430d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4430d-137">CommonParameters</span></span>
<span data-ttu-id="4430d-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4430d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4430d-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4430d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4430d-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4430d-140">INPUTS</span></span>

### <span data-ttu-id="4430d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4430d-141">System.String</span></span>

## <span data-ttu-id="4430d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4430d-142">OUTPUTS</span></span>

### <span data-ttu-id="4430d-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="4430d-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="4430d-144">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="4430d-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="4430d-145">Note</span><span class="sxs-lookup"><span data-stu-id="4430d-145">NOTES</span></span>

## <span data-ttu-id="4430d-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4430d-146">RELATED LINKS</span></span>

[<span data-ttu-id="4430d-147">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4430d-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="4430d-148">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4430d-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="4430d-149">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4430d-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="4430d-150">Salva-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4430d-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


