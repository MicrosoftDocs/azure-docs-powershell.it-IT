---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 809246520c4e6b07a1aca406ef3ec17eb9df31f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863786"
---
# <span data-ttu-id="2da3d-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="2da3d-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="2da3d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2da3d-102">SYNOPSIS</span></span>
<span data-ttu-id="2da3d-103">Ottiene informazioni su un'estensione del dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2da3d-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="2da3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2da3d-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2da3d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2da3d-105">DESCRIPTION</span></span>
<span data-ttu-id="2da3d-106">Il cmdlet **Get-AzVMADDomainExtension** ottiene le informazioni sull'estensione di dominio di Azure Active Directory specificata (ad).</span><span class="sxs-lookup"><span data-stu-id="2da3d-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="2da3d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2da3d-107">EXAMPLES</span></span>

### <span data-ttu-id="2da3d-108">1:</span><span class="sxs-lookup"><span data-stu-id="2da3d-108">1:</span></span>
```

```

## <span data-ttu-id="2da3d-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2da3d-109">PARAMETERS</span></span>

### <span data-ttu-id="2da3d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da3d-110">-DefaultProfile</span></span>
<span data-ttu-id="2da3d-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2da3d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2da3d-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="2da3d-112">-Name</span></span>
<span data-ttu-id="2da3d-113">Specifica il nome dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="2da3d-113">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="2da3d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2da3d-114">-ResourceGroupName</span></span>
<span data-ttu-id="2da3d-115">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2da3d-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2da3d-116">-Stato</span><span class="sxs-lookup"><span data-stu-id="2da3d-116">-Status</span></span>
<span data-ttu-id="2da3d-117">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="2da3d-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="2da3d-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="2da3d-118">-VMName</span></span>
<span data-ttu-id="2da3d-119">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2da3d-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="2da3d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da3d-120">CommonParameters</span></span>
<span data-ttu-id="2da3d-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2da3d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da3d-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2da3d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da3d-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2da3d-123">INPUTS</span></span>

### <span data-ttu-id="2da3d-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2da3d-124">None</span></span>
<span data-ttu-id="2da3d-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2da3d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2da3d-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2da3d-126">OUTPUTS</span></span>

### <span data-ttu-id="2da3d-127">Microsoft. Azure. Commands. Compute. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="2da3d-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="2da3d-128">Note</span><span class="sxs-lookup"><span data-stu-id="2da3d-128">NOTES</span></span>

## <span data-ttu-id="2da3d-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2da3d-129">RELATED LINKS</span></span>

[<span data-ttu-id="2da3d-130">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="2da3d-130">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


