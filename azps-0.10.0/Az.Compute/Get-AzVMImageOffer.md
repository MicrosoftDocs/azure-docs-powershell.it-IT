---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: eb56542d02498a0d4b8aa4176c77d75ab6ad4da6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863734"
---
# <span data-ttu-id="ea0c4-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="ea0c4-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="ea0c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0c4-103">Ottiene i tipi di offerta di VMImage.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="ea0c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea0c4-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea0c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea0c4-105">DESCRIPTION</span></span>
<span data-ttu-id="ea0c4-106">Il cmdlet **Get-AzVMImageOffer** ottiene i tipi di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="ea0c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea0c4-107">EXAMPLES</span></span>

### <span data-ttu-id="ea0c4-108">Esempio 1: ottenere tipi di offerta per un autore</span><span class="sxs-lookup"><span data-stu-id="ea0c4-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="ea0c4-109">Questo comando consente di ottenere i tipi di offerta per l'autore specificato nell'area centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="ea0c4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea0c4-110">PARAMETERS</span></span>

### <span data-ttu-id="ea0c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0c4-111">-DefaultProfile</span></span>
<span data-ttu-id="ea0c4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea0c4-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ea0c4-113">-Location</span></span>
<span data-ttu-id="ea0c4-114">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="ea0c4-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="ea0c4-115">-PublisherName</span></span>
<span data-ttu-id="ea0c4-116">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="ea0c4-117">Per ottenere un autore, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="ea0c4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0c4-118">CommonParameters</span></span>
<span data-ttu-id="ea0c4-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0c4-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea0c4-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0c4-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea0c4-121">INPUTS</span></span>

### <span data-ttu-id="ea0c4-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ea0c4-122">None</span></span>
<span data-ttu-id="ea0c4-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea0c4-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea0c4-124">OUTPUTS</span></span>

### <span data-ttu-id="ea0c4-125">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="ea0c4-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="ea0c4-126">Note</span><span class="sxs-lookup"><span data-stu-id="ea0c4-126">NOTES</span></span>

## <span data-ttu-id="ea0c4-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea0c4-127">RELATED LINKS</span></span>

[<span data-ttu-id="ea0c4-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ea0c4-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="ea0c4-129">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ea0c4-129">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="ea0c4-130">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="ea0c4-130">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="ea0c4-131">Salva-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ea0c4-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


