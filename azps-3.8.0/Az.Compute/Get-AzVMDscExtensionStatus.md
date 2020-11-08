---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: 9b35e76b6c64373a39bd3e14f8c1697c7c5f3baf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020852"
---
# <span data-ttu-id="285b2-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="285b2-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="285b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="285b2-102">SYNOPSIS</span></span>
<span data-ttu-id="285b2-103">Ottiene lo stato del gestore dell'estensione DSC per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="285b2-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="285b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="285b2-104">SYNTAX</span></span>

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="285b2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="285b2-105">DESCRIPTION</span></span>
<span data-ttu-id="285b2-106">Il cmdlet **Get-AzVMDscExtensionStatus** ottiene lo stato del gestore di estensione DSC (Desired state Configuration) per una macchina virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="285b2-106">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="285b2-107">Quando viene applicata una configurazione, questo cmdlet produce l'output coerente con il cmdlet Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="285b2-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="285b2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="285b2-108">EXAMPLES</span></span>

## <span data-ttu-id="285b2-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="285b2-109">PARAMETERS</span></span>

### <span data-ttu-id="285b2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285b2-110">-DefaultProfile</span></span>
<span data-ttu-id="285b2-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="285b2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="285b2-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="285b2-112">-Name</span></span>
<span data-ttu-id="285b2-113">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="285b2-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="285b2-114">Il cmdlet Set-AzVMDscExtension imposta questo nome su Microsoft. PowerShell. DSC, che è lo stesso valore usato da **Get-AzVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="285b2-114">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="285b2-115">Specificare questo parametro solo se è stato modificato il nome predefinito nel cmdlet Set o si è usato un nome di risorsa diverso in un modello di gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="285b2-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285b2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="285b2-116">-ResourceGroupName</span></span>
<span data-ttu-id="285b2-117">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="285b2-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="285b2-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="285b2-118">-VMName</span></span>
<span data-ttu-id="285b2-119">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene lo stato dell'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="285b2-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285b2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285b2-120">CommonParameters</span></span>
<span data-ttu-id="285b2-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="285b2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285b2-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="285b2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285b2-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="285b2-123">INPUTS</span></span>

### <span data-ttu-id="285b2-124">System. String</span><span class="sxs-lookup"><span data-stu-id="285b2-124">System.String</span></span>

## <span data-ttu-id="285b2-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="285b2-125">OUTPUTS</span></span>

### <span data-ttu-id="285b2-126">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="285b2-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="285b2-127">Note</span><span class="sxs-lookup"><span data-stu-id="285b2-127">NOTES</span></span>

## <span data-ttu-id="285b2-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="285b2-128">RELATED LINKS</span></span>

[<span data-ttu-id="285b2-129">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="285b2-129">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


