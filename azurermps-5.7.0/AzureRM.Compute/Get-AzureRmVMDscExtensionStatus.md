---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 7cb7f175cc15e7d4e0915b6af9ef6fe6bdfc74d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510016"
---
# <span data-ttu-id="5f453-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="5f453-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="5f453-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f453-102">SYNOPSIS</span></span>
<span data-ttu-id="5f453-103">Ottiene lo stato del gestore dell'estensione DSC per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5f453-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f453-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f453-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f453-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f453-105">DESCRIPTION</span></span>
<span data-ttu-id="5f453-106">Il cmdlet **Get-AzureRmVMDscExtensionStatus** ottiene lo stato del gestore di estensione DSC (Desired state Configuration) per una macchina virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5f453-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="5f453-107">Quando viene applicata una configurazione, questo cmdlet produce l'output coerente con il cmdlet Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5f453-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="5f453-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f453-108">EXAMPLES</span></span>

## <span data-ttu-id="5f453-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f453-109">PARAMETERS</span></span>

### <span data-ttu-id="5f453-110">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f453-110">-Name</span></span>
<span data-ttu-id="5f453-111">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="5f453-111">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="5f453-112">Il cmdlet Set-AzureRmVMDscExtension imposta questo nome su Microsoft. PowerShell. DSC, che è lo stesso valore usato da **Get-AzureRmVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="5f453-112">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="5f453-113">Specificare questo parametro solo se è stato modificato il nome predefinito nel cmdlet Set o si è usato un nome di risorsa diverso in un modello di gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="5f453-113">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="5f453-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f453-114">-ResourceGroupName</span></span>
<span data-ttu-id="5f453-115">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5f453-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5f453-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="5f453-116">-VMName</span></span>
<span data-ttu-id="5f453-117">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene lo stato dell'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="5f453-117">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="5f453-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f453-118">CommonParameters</span></span>
<span data-ttu-id="5f453-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f453-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f453-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f453-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f453-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f453-121">INPUTS</span></span>

### <span data-ttu-id="5f453-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5f453-122">None</span></span>
<span data-ttu-id="5f453-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5f453-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f453-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f453-124">OUTPUTS</span></span>

## <span data-ttu-id="5f453-125">Note</span><span class="sxs-lookup"><span data-stu-id="5f453-125">NOTES</span></span>

## <span data-ttu-id="5f453-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f453-126">RELATED LINKS</span></span>

[<span data-ttu-id="5f453-127">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="5f453-127">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


