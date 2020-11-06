---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: 398cc4b8f23ca5296aec741eb720833f589b0e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511863"
---
# <span data-ttu-id="32fdc-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="32fdc-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="32fdc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="32fdc-103">Ottiene informazioni su un'estensione del dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="32fdc-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32fdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32fdc-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32fdc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32fdc-105">DESCRIPTION</span></span>
<span data-ttu-id="32fdc-106">Il cmdlet **Get-AzureRmVMADDomainExtension** ottiene le informazioni sull'estensione di dominio di Azure Active Directory specificata (ad).</span><span class="sxs-lookup"><span data-stu-id="32fdc-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="32fdc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32fdc-107">EXAMPLES</span></span>

## <span data-ttu-id="32fdc-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32fdc-108">PARAMETERS</span></span>

### <span data-ttu-id="32fdc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32fdc-109">-DefaultProfile</span></span>
<span data-ttu-id="32fdc-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32fdc-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32fdc-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="32fdc-111">-Name</span></span>
<span data-ttu-id="32fdc-112">Specifica il nome dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="32fdc-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="32fdc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32fdc-113">-ResourceGroupName</span></span>
<span data-ttu-id="32fdc-114">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="32fdc-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="32fdc-115">-Stato</span><span class="sxs-lookup"><span data-stu-id="32fdc-115">-Status</span></span>
<span data-ttu-id="32fdc-116">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="32fdc-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="32fdc-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="32fdc-117">-VMName</span></span>
<span data-ttu-id="32fdc-118">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32fdc-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="32fdc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32fdc-119">CommonParameters</span></span>
<span data-ttu-id="32fdc-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32fdc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32fdc-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32fdc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32fdc-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32fdc-122">INPUTS</span></span>

### <span data-ttu-id="32fdc-123">System. String</span><span class="sxs-lookup"><span data-stu-id="32fdc-123">System.String</span></span>

### <span data-ttu-id="32fdc-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="32fdc-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="32fdc-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32fdc-125">OUTPUTS</span></span>

### <span data-ttu-id="32fdc-126">Microsoft. Azure. Commands. Compute. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="32fdc-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="32fdc-127">Note</span><span class="sxs-lookup"><span data-stu-id="32fdc-127">NOTES</span></span>

## <span data-ttu-id="32fdc-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32fdc-128">RELATED LINKS</span></span>

[<span data-ttu-id="32fdc-129">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="32fdc-129">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


