---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 13871100efbe2fe62de769adcc40ee434e86eb21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852114"
---
# <span data-ttu-id="32fe1-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="32fe1-101">Get-AzVMImage</span></span>

## <span data-ttu-id="32fe1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32fe1-102">SYNOPSIS</span></span>
<span data-ttu-id="32fe1-103">Ottiene tutte le versioni di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="32fe1-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="32fe1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32fe1-104">SYNTAX</span></span>

### <span data-ttu-id="32fe1-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="32fe1-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32fe1-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="32fe1-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32fe1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32fe1-107">DESCRIPTION</span></span>
<span data-ttu-id="32fe1-108">Il cmdlet **Get-AzVMImage** ottiene tutte le versioni di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="32fe1-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="32fe1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32fe1-109">EXAMPLES</span></span>

### <span data-ttu-id="32fe1-110">Esempio 1: ottenere oggetti VMImage</span><span class="sxs-lookup"><span data-stu-id="32fe1-110">Example 1: Get VMImage objects</span></span>
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

<span data-ttu-id="32fe1-111">Questo comando consente di ottenere tutte le versioni di VMImage che corrispondono ai valori specificati.</span><span class="sxs-lookup"><span data-stu-id="32fe1-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="32fe1-112">Esempio 2: ottenere l'oggetto VMImage</span><span class="sxs-lookup"><span data-stu-id="32fe1-112">Example 2: Get VMImage object</span></span>
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

<span data-ttu-id="32fe1-113">Questo comando ottiene una versione specifica di VMImage che corrisponde ai valori specificati.</span><span class="sxs-lookup"><span data-stu-id="32fe1-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="32fe1-114">Esempio 3: ottenere oggetti VMImage</span><span class="sxs-lookup"><span data-stu-id="32fe1-114">Example 3: Get VMImage objects</span></span>
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

<span data-ttu-id="32fe1-115">Questo comando consente di ottenere tutte le versioni di VMImage che corrispondono ai valori specificati con il filtro sulla versione.</span><span class="sxs-lookup"><span data-stu-id="32fe1-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="32fe1-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32fe1-116">PARAMETERS</span></span>

### <span data-ttu-id="32fe1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32fe1-117">-DefaultProfile</span></span>
<span data-ttu-id="32fe1-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32fe1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32fe1-119">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="32fe1-119">-FilterExpression</span></span>
<span data-ttu-id="32fe1-120">Specifica un'espressione di filtro.</span><span class="sxs-lookup"><span data-stu-id="32fe1-120">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32fe1-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="32fe1-121">-Location</span></span>
<span data-ttu-id="32fe1-122">Specifica la posizione di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="32fe1-122">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="32fe1-123">-Offerta</span><span class="sxs-lookup"><span data-stu-id="32fe1-123">-Offer</span></span>
<span data-ttu-id="32fe1-124">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="32fe1-124">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="32fe1-125">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="32fe1-125">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="32fe1-126">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="32fe1-126">-PublisherName</span></span>
<span data-ttu-id="32fe1-127">Specifica l'autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="32fe1-127">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="32fe1-128">Per ottenere un autore di immagini, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="32fe1-128">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="32fe1-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="32fe1-129">-Skus</span></span>
<span data-ttu-id="32fe1-130">Specifica una SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="32fe1-130">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="32fe1-131">Per ottenere un SKU, usare il cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="32fe1-131">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="32fe1-132">-Versione</span><span class="sxs-lookup"><span data-stu-id="32fe1-132">-Version</span></span>
<span data-ttu-id="32fe1-133">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="32fe1-133">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="32fe1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32fe1-134">CommonParameters</span></span>
<span data-ttu-id="32fe1-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32fe1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32fe1-136">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32fe1-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32fe1-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32fe1-137">INPUTS</span></span>

### <span data-ttu-id="32fe1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="32fe1-138">System.String</span></span>

## <span data-ttu-id="32fe1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32fe1-139">OUTPUTS</span></span>

### <span data-ttu-id="32fe1-140">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="32fe1-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="32fe1-141">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="32fe1-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="32fe1-142">Note</span><span class="sxs-lookup"><span data-stu-id="32fe1-142">NOTES</span></span>

## <span data-ttu-id="32fe1-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32fe1-143">RELATED LINKS</span></span>

[<span data-ttu-id="32fe1-144">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="32fe1-144">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="32fe1-145">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="32fe1-145">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="32fe1-146">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="32fe1-146">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="32fe1-147">Salva-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="32fe1-147">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


