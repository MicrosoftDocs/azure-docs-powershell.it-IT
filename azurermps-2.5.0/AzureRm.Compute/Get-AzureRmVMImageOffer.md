---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimageoffer
schema: 2.0.0
ms.openlocfilehash: 00169d833244ece2f697d2429f5e5db5ee0bf901
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866372"
---
# <span data-ttu-id="9b4a7-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9b4a7-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="9b4a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b4a7-102">SYNOPSIS</span></span>
<span data-ttu-id="9b4a7-103">Ottiene i tipi di offerta di VMImage.</span><span class="sxs-lookup"><span data-stu-id="9b4a7-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b4a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b4a7-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b4a7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b4a7-105">DESCRIPTION</span></span>
<span data-ttu-id="9b4a7-106">Il cmdlet **Get-AzureRmVMImageOffer** ottiene i tipi di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="9b4a7-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="9b4a7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b4a7-107">EXAMPLES</span></span>

### <span data-ttu-id="9b4a7-108">Esempio 1: ottenere tipi di offerta per un autore</span><span class="sxs-lookup"><span data-stu-id="9b4a7-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="9b4a7-109">Questo comando consente di ottenere i tipi di offerta per l'autore specificato nell'area centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="9b4a7-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="9b4a7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b4a7-110">PARAMETERS</span></span>

### <span data-ttu-id="9b4a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b4a7-111">-DefaultProfile</span></span>
<span data-ttu-id="9b4a7-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b4a7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b4a7-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9b4a7-113">-Location</span></span>
<span data-ttu-id="9b4a7-114">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="9b4a7-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="9b4a7-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9b4a7-115">-PublisherName</span></span>
<span data-ttu-id="9b4a7-116">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="9b4a7-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="9b4a7-117">Per ottenere un autore, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="9b4a7-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9b4a7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b4a7-118">CommonParameters</span></span>
<span data-ttu-id="9b4a7-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b4a7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b4a7-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b4a7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b4a7-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b4a7-121">INPUTS</span></span>

### <span data-ttu-id="9b4a7-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9b4a7-122">None</span></span>
<span data-ttu-id="9b4a7-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9b4a7-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9b4a7-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b4a7-124">OUTPUTS</span></span>

### <span data-ttu-id="9b4a7-125">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="9b4a7-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="9b4a7-126">Note</span><span class="sxs-lookup"><span data-stu-id="9b4a7-126">NOTES</span></span>

## <span data-ttu-id="9b4a7-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b4a7-127">RELATED LINKS</span></span>

[<span data-ttu-id="9b4a7-128">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9b4a7-128">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="9b4a7-129">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9b4a7-129">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="9b4a7-130">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9b4a7-130">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="9b4a7-131">Salva-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9b4a7-131">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


