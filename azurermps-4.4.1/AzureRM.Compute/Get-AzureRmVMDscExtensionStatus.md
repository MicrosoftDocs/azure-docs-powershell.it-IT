---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 0a14bf4f2c8a4b686f222079cadaec1744e41d08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519610"
---
# <span data-ttu-id="88e22-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="88e22-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="88e22-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88e22-102">SYNOPSIS</span></span>
<span data-ttu-id="88e22-103">Ottiene lo stato del gestore dell'estensione DSC per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="88e22-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88e22-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88e22-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88e22-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88e22-105">DESCRIPTION</span></span>
<span data-ttu-id="88e22-106">Il cmdlet **Get-AzureRmVMDscExtensionStatus** ottiene lo stato del gestore di estensione DSC (Desired state Configuration) per una macchina virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="88e22-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="88e22-107">Quando viene applicata una configurazione, questo cmdlet produce l'output coerente con il cmdlet Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="88e22-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="88e22-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88e22-108">EXAMPLES</span></span>

## <span data-ttu-id="88e22-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88e22-109">PARAMETERS</span></span>

### <span data-ttu-id="88e22-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e22-110">-DefaultProfile</span></span>
<span data-ttu-id="88e22-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88e22-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88e22-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="88e22-112">-Name</span></span>
<span data-ttu-id="88e22-113">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="88e22-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="88e22-114">Il cmdlet Set-AzureRmVMDscExtension imposta questo nome su Microsoft. PowerShell. DSC, che è lo stesso valore usato da **Get-AzureRmVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="88e22-114">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="88e22-115">Specificare questo parametro solo se è stato modificato il nome predefinito nel cmdlet Set o si è usato un nome di risorsa diverso in un modello di gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="88e22-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="88e22-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88e22-116">-ResourceGroupName</span></span>
<span data-ttu-id="88e22-117">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="88e22-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="88e22-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="88e22-118">-VMName</span></span>
<span data-ttu-id="88e22-119">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene lo stato dell'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="88e22-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="88e22-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e22-120">CommonParameters</span></span>
<span data-ttu-id="88e22-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88e22-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e22-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e22-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e22-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88e22-123">INPUTS</span></span>

## <span data-ttu-id="88e22-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88e22-124">OUTPUTS</span></span>

## <span data-ttu-id="88e22-125">Note</span><span class="sxs-lookup"><span data-stu-id="88e22-125">NOTES</span></span>

## <span data-ttu-id="88e22-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88e22-126">RELATED LINKS</span></span>

[<span data-ttu-id="88e22-127">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="88e22-127">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


