---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: d55d84560ca75a508a05276d8d33eb78d1d50ab5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516880"
---
# <span data-ttu-id="e010e-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="e010e-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="e010e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e010e-102">SYNOPSIS</span></span>
<span data-ttu-id="e010e-103">Ottiene informazioni su un'estensione del dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e010e-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e010e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e010e-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="e010e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e010e-105">DESCRIPTION</span></span>
<span data-ttu-id="e010e-106">Il cmdlet **Get-AzureRmVMADDomainExtension** ottiene le informazioni sull'estensione di dominio di Azure Active Directory specificata (ad).</span><span class="sxs-lookup"><span data-stu-id="e010e-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="e010e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e010e-107">EXAMPLES</span></span>

## <span data-ttu-id="e010e-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e010e-108">PARAMETERS</span></span>

### <span data-ttu-id="e010e-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="e010e-109">-Name</span></span>
<span data-ttu-id="e010e-110">Specifica il nome dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="e010e-110">Specifies the name of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e010e-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e010e-111">-ResourceGroupName</span></span>
<span data-ttu-id="e010e-112">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e010e-112">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e010e-113">-Stato</span><span class="sxs-lookup"><span data-stu-id="e010e-113">-Status</span></span>
<span data-ttu-id="e010e-114">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="e010e-114">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e010e-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="e010e-115">-VMName</span></span>
<span data-ttu-id="e010e-116">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e010e-116">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e010e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e010e-117">CommonParameters</span></span>
<span data-ttu-id="e010e-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e010e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e010e-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e010e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e010e-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e010e-120">INPUTS</span></span>

### <span data-ttu-id="e010e-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e010e-121">None</span></span>
<span data-ttu-id="e010e-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e010e-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e010e-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e010e-123">OUTPUTS</span></span>

## <span data-ttu-id="e010e-124">Note</span><span class="sxs-lookup"><span data-stu-id="e010e-124">NOTES</span></span>

## <span data-ttu-id="e010e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e010e-125">RELATED LINKS</span></span>

[<span data-ttu-id="e010e-126">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="e010e-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


