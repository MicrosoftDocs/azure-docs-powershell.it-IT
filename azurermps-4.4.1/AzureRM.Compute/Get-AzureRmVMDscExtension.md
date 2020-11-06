---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
ms.openlocfilehash: ea54fc227fb32fe945a7a5ccc33133fc3b1d98a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519611"
---
# <span data-ttu-id="d67d2-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d67d2-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="d67d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d67d2-102">SYNOPSIS</span></span>
<span data-ttu-id="d67d2-103">Ottiene le impostazioni dell'estensione DSC in una particolare macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d67d2-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d67d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d67d2-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d67d2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d67d2-105">DESCRIPTION</span></span>
<span data-ttu-id="d67d2-106">Il cmdlet **Get-AzureRmVMDscExtension** ottiene le impostazioni dell'estensione di configurazione dello stato desiderata in una determinata macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d67d2-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="d67d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d67d2-107">EXAMPLES</span></span>

### <span data-ttu-id="d67d2-108">Esempio 1: ottenere le impostazioni di un'estensione DSC</span><span class="sxs-lookup"><span data-stu-id="d67d2-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="d67d2-109">Questo comando consente di ottenere le impostazioni di estensione denominate DSC nella macchina virtuale denominata VM07.</span><span class="sxs-lookup"><span data-stu-id="d67d2-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="d67d2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d67d2-110">PARAMETERS</span></span>

### <span data-ttu-id="d67d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67d2-111">-DefaultProfile</span></span>
<span data-ttu-id="d67d2-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d67d2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d67d2-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d67d2-113">-Name</span></span>
<span data-ttu-id="d67d2-114">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="d67d2-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="d67d2-115">Il cmdlet Set-AzureRmVMDscExtension imposta questo nome su Microsoft. PowerShell. DSC, che è lo stesso valore usato da **Get-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="d67d2-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="d67d2-116">Specifica questo parametro solo se il nome predefinito è stato modificato nel cmdlet **set-AzureRmVMDscExtension** o si usa un nome di risorsa diverso in un modello di gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="d67d2-116">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="d67d2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d67d2-117">-ResourceGroupName</span></span>
<span data-ttu-id="d67d2-118">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d67d2-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d67d2-119">-Stato</span><span class="sxs-lookup"><span data-stu-id="d67d2-119">-Status</span></span>
<span data-ttu-id="d67d2-120">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="d67d2-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67d2-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="d67d2-121">-VMName</span></span>
<span data-ttu-id="d67d2-122">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene l'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="d67d2-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="d67d2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67d2-123">CommonParameters</span></span>
<span data-ttu-id="d67d2-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d67d2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67d2-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d67d2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67d2-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d67d2-126">INPUTS</span></span>

## <span data-ttu-id="d67d2-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d67d2-127">OUTPUTS</span></span>

### <span data-ttu-id="d67d2-128">Microsoft. Azure. Commands. Compute. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d67d2-128">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="d67d2-129">Note</span><span class="sxs-lookup"><span data-stu-id="d67d2-129">NOTES</span></span>

## <span data-ttu-id="d67d2-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d67d2-130">RELATED LINKS</span></span>

[<span data-ttu-id="d67d2-131">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d67d2-131">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="d67d2-132">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d67d2-132">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


