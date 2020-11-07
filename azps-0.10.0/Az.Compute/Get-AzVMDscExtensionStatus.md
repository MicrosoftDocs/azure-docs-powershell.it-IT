---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: 3ae9827c6db5136b9327936a63ac0441dcf94ff1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863749"
---
# <span data-ttu-id="3c0ba-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="3c0ba-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="3c0ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c0ba-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0ba-103">Ottiene lo stato del gestore dell'estensione DSC per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3c0ba-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="3c0ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c0ba-104">SYNTAX</span></span>

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c0ba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c0ba-105">DESCRIPTION</span></span>
<span data-ttu-id="3c0ba-106">Il cmdlet **Get-AzVMDscExtensionStatus** ottiene lo stato del gestore di estensione DSC (Desired state Configuration) per una macchina virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3c0ba-106">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="3c0ba-107">Quando viene applicata una configurazione, questo cmdlet produce l'output coerente con il cmdlet Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3c0ba-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="3c0ba-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c0ba-108">EXAMPLES</span></span>

### <span data-ttu-id="3c0ba-109">1:</span><span class="sxs-lookup"><span data-stu-id="3c0ba-109">1:</span></span>
```

```

## <span data-ttu-id="3c0ba-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c0ba-110">PARAMETERS</span></span>

### <span data-ttu-id="3c0ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0ba-111">-DefaultProfile</span></span>
<span data-ttu-id="3c0ba-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c0ba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c0ba-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c0ba-113">-Name</span></span>
<span data-ttu-id="3c0ba-114">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="3c0ba-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="3c0ba-115">Il cmdlet Set-AzVMDscExtension imposta questo nome su Microsoft. PowerShell. DSC, che è lo stesso valore usato da **Get-AzVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="3c0ba-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="3c0ba-116">Specificare questo parametro solo se è stato modificato il nome predefinito nel cmdlet Set o si è usato un nome di risorsa diverso in un modello di gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="3c0ba-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c0ba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c0ba-117">-ResourceGroupName</span></span>
<span data-ttu-id="3c0ba-118">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3c0ba-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3c0ba-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="3c0ba-119">-VMName</span></span>
<span data-ttu-id="3c0ba-120">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene lo stato dell'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="3c0ba-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c0ba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0ba-121">CommonParameters</span></span>
<span data-ttu-id="3c0ba-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c0ba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0ba-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c0ba-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0ba-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c0ba-124">INPUTS</span></span>

### <span data-ttu-id="3c0ba-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3c0ba-125">None</span></span>
<span data-ttu-id="3c0ba-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3c0ba-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3c0ba-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c0ba-127">OUTPUTS</span></span>

### <span data-ttu-id="3c0ba-128">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="3c0ba-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="3c0ba-129">Note</span><span class="sxs-lookup"><span data-stu-id="3c0ba-129">NOTES</span></span>

## <span data-ttu-id="3c0ba-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c0ba-130">RELATED LINKS</span></span>

[<span data-ttu-id="3c0ba-131">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="3c0ba-131">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


