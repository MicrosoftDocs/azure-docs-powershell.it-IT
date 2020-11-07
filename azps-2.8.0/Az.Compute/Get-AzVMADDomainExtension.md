---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 2ec4ec1898e79fd7f7f35a406f2a99f9dd2da6fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675415"
---
# <span data-ttu-id="2757e-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="2757e-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="2757e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2757e-102">SYNOPSIS</span></span>
<span data-ttu-id="2757e-103">Ottiene informazioni su un'estensione del dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2757e-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="2757e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2757e-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2757e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2757e-105">DESCRIPTION</span></span>
<span data-ttu-id="2757e-106">Il cmdlet **Get-AzVMADDomainExtension** ottiene le informazioni sull'estensione di dominio di Azure Active Directory specificata (ad).</span><span class="sxs-lookup"><span data-stu-id="2757e-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="2757e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2757e-107">EXAMPLES</span></span>

## <span data-ttu-id="2757e-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2757e-108">PARAMETERS</span></span>

### <span data-ttu-id="2757e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2757e-109">-DefaultProfile</span></span>
<span data-ttu-id="2757e-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2757e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2757e-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="2757e-111">-Name</span></span>
<span data-ttu-id="2757e-112">Specifica il nome dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="2757e-112">Specifies the name of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2757e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2757e-113">-ResourceGroupName</span></span>
<span data-ttu-id="2757e-114">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2757e-114">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2757e-115">-Stato</span><span class="sxs-lookup"><span data-stu-id="2757e-115">-Status</span></span>
<span data-ttu-id="2757e-116">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="2757e-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2757e-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="2757e-117">-VMName</span></span>
<span data-ttu-id="2757e-118">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2757e-118">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2757e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2757e-119">CommonParameters</span></span>
<span data-ttu-id="2757e-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2757e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2757e-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2757e-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2757e-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2757e-122">INPUTS</span></span>

### <span data-ttu-id="2757e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2757e-123">System.String</span></span>

### <span data-ttu-id="2757e-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2757e-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2757e-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2757e-125">OUTPUTS</span></span>

### <span data-ttu-id="2757e-126">Microsoft. Azure. Commands. Compute. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="2757e-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="2757e-127">Note</span><span class="sxs-lookup"><span data-stu-id="2757e-127">NOTES</span></span>

## <span data-ttu-id="2757e-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2757e-128">RELATED LINKS</span></span>

[<span data-ttu-id="2757e-129">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="2757e-129">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)

