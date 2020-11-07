---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
ms.openlocfilehash: 01a5a69053cfd05186abae45d5b53fff0b022b98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866135"
---
# <span data-ttu-id="f306a-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f306a-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="f306a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f306a-102">SYNOPSIS</span></span>
<span data-ttu-id="f306a-103">Ottiene informazioni su un'estensione del dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f306a-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f306a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f306a-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f306a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f306a-105">DESCRIPTION</span></span>
<span data-ttu-id="f306a-106">Il cmdlet **Get-AzureRmVMADDomainExtension** ottiene le informazioni sull'estensione di dominio di Azure Active Directory specificata (ad).</span><span class="sxs-lookup"><span data-stu-id="f306a-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="f306a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f306a-107">EXAMPLES</span></span>

### <span data-ttu-id="f306a-108">1:</span><span class="sxs-lookup"><span data-stu-id="f306a-108">1:</span></span>
```

```

## <span data-ttu-id="f306a-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f306a-109">PARAMETERS</span></span>

### <span data-ttu-id="f306a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f306a-110">-DefaultProfile</span></span>
<span data-ttu-id="f306a-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f306a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f306a-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="f306a-112">-Name</span></span>
<span data-ttu-id="f306a-113">Specifica il nome dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="f306a-113">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="f306a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f306a-114">-ResourceGroupName</span></span>
<span data-ttu-id="f306a-115">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f306a-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f306a-116">-Stato</span><span class="sxs-lookup"><span data-stu-id="f306a-116">-Status</span></span>
<span data-ttu-id="f306a-117">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="f306a-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="f306a-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="f306a-118">-VMName</span></span>
<span data-ttu-id="f306a-119">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f306a-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="f306a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f306a-120">CommonParameters</span></span>
<span data-ttu-id="f306a-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f306a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f306a-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f306a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f306a-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f306a-123">INPUTS</span></span>

### <span data-ttu-id="f306a-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f306a-124">None</span></span>
<span data-ttu-id="f306a-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f306a-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f306a-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f306a-126">OUTPUTS</span></span>

### <span data-ttu-id="f306a-127">Microsoft. Azure. Commands. Compute. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="f306a-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="f306a-128">Note</span><span class="sxs-lookup"><span data-stu-id="f306a-128">NOTES</span></span>

## <span data-ttu-id="f306a-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f306a-129">RELATED LINKS</span></span>

[<span data-ttu-id="f306a-130">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f306a-130">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


