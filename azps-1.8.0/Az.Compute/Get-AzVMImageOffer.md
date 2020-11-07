---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: 5ec6b8c01badec3677e77254128db215c0e41554
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852113"
---
# <span data-ttu-id="ee873-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="ee873-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="ee873-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee873-102">SYNOPSIS</span></span>
<span data-ttu-id="ee873-103">Ottiene i tipi di offerta di VMImage.</span><span class="sxs-lookup"><span data-stu-id="ee873-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="ee873-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee873-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee873-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee873-105">DESCRIPTION</span></span>
<span data-ttu-id="ee873-106">Il cmdlet **Get-AzVMImageOffer** ottiene i tipi di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="ee873-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="ee873-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee873-107">EXAMPLES</span></span>

### <span data-ttu-id="ee873-108">Esempio 1: ottenere tipi di offerta per un autore</span><span class="sxs-lookup"><span data-stu-id="ee873-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="ee873-109">Questo comando consente di ottenere i tipi di offerta per l'autore specificato nell'area centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="ee873-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="ee873-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee873-110">PARAMETERS</span></span>

### <span data-ttu-id="ee873-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee873-111">-DefaultProfile</span></span>
<span data-ttu-id="ee873-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee873-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee873-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ee873-113">-Location</span></span>
<span data-ttu-id="ee873-114">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="ee873-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="ee873-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="ee873-115">-PublisherName</span></span>
<span data-ttu-id="ee873-116">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="ee873-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="ee873-117">Per ottenere un autore, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="ee873-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="ee873-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee873-118">CommonParameters</span></span>
<span data-ttu-id="ee873-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee873-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee873-120">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee873-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee873-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee873-121">INPUTS</span></span>

### <span data-ttu-id="ee873-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ee873-122">System.String</span></span>

## <span data-ttu-id="ee873-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee873-123">OUTPUTS</span></span>

### <span data-ttu-id="ee873-124">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="ee873-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="ee873-125">Note</span><span class="sxs-lookup"><span data-stu-id="ee873-125">NOTES</span></span>

## <span data-ttu-id="ee873-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee873-126">RELATED LINKS</span></span>

[<span data-ttu-id="ee873-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ee873-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="ee873-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ee873-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="ee873-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="ee873-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="ee873-130">Salva-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ee873-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


