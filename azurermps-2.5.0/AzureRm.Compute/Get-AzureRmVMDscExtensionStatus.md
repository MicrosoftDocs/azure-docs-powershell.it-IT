---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextensionstatus
schema: 2.0.0
ms.openlocfilehash: b6ec9918657c191e31e10c04b799603654d39d56
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865852"
---
# <span data-ttu-id="f41ee-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="f41ee-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="f41ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f41ee-102">SYNOPSIS</span></span>
<span data-ttu-id="f41ee-103">Ottiene lo stato del gestore dell'estensione DSC per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f41ee-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f41ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f41ee-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f41ee-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f41ee-105">DESCRIPTION</span></span>
<span data-ttu-id="f41ee-106">Il cmdlet **Get-AzureRmVMDscExtensionStatus** ottiene lo stato del gestore di estensione DSC (Desired state Configuration) per una macchina virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f41ee-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="f41ee-107">Quando viene applicata una configurazione, questo cmdlet produce l'output coerente con il cmdlet Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f41ee-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="f41ee-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f41ee-108">EXAMPLES</span></span>

### <span data-ttu-id="f41ee-109">1:</span><span class="sxs-lookup"><span data-stu-id="f41ee-109">1:</span></span>
```

```

## <span data-ttu-id="f41ee-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f41ee-110">PARAMETERS</span></span>

### <span data-ttu-id="f41ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f41ee-111">-DefaultProfile</span></span>
<span data-ttu-id="f41ee-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f41ee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f41ee-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f41ee-113">-Name</span></span>
<span data-ttu-id="f41ee-114">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="f41ee-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="f41ee-115">Il cmdlet Set-AzureRmVMDscExtension imposta questo nome su Microsoft. PowerShell. DSC, che è lo stesso valore usato da **Get-AzureRmVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="f41ee-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="f41ee-116">Specificare questo parametro solo se è stato modificato il nome predefinito nel cmdlet Set o si è usato un nome di risorsa diverso in un modello di gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="f41ee-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="f41ee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f41ee-117">-ResourceGroupName</span></span>
<span data-ttu-id="f41ee-118">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f41ee-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f41ee-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="f41ee-119">-VMName</span></span>
<span data-ttu-id="f41ee-120">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene lo stato dell'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="f41ee-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="f41ee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f41ee-121">CommonParameters</span></span>
<span data-ttu-id="f41ee-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f41ee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f41ee-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f41ee-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f41ee-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f41ee-124">INPUTS</span></span>

### <span data-ttu-id="f41ee-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f41ee-125">None</span></span>
<span data-ttu-id="f41ee-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f41ee-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f41ee-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f41ee-127">OUTPUTS</span></span>

### <span data-ttu-id="f41ee-128">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="f41ee-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="f41ee-129">Note</span><span class="sxs-lookup"><span data-stu-id="f41ee-129">NOTES</span></span>

## <span data-ttu-id="f41ee-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f41ee-130">RELATED LINKS</span></span>

[<span data-ttu-id="f41ee-131">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f41ee-131">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


