---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: 0ae022c9a8755c0ffa8bdfeafa12ab18922214a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684809"
---
# <span data-ttu-id="479fb-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="479fb-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="479fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="479fb-102">SYNOPSIS</span></span>
<span data-ttu-id="479fb-103">Ottiene le impostazioni dell'estensione DSC in una particolare macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="479fb-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="479fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="479fb-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="479fb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="479fb-105">DESCRIPTION</span></span>
<span data-ttu-id="479fb-106">Il cmdlet **Get-AzVMDscExtension** ottiene le impostazioni dell'estensione di configurazione dello stato desiderata in una determinata macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="479fb-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="479fb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="479fb-107">EXAMPLES</span></span>

### <span data-ttu-id="479fb-108">Esempio 1: ottenere le impostazioni di un'estensione DSC</span><span class="sxs-lookup"><span data-stu-id="479fb-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="479fb-109">Questo comando consente di ottenere le impostazioni di estensione denominate DSC nella macchina virtuale denominata VM07.</span><span class="sxs-lookup"><span data-stu-id="479fb-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="479fb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="479fb-110">PARAMETERS</span></span>

### <span data-ttu-id="479fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="479fb-111">-DefaultProfile</span></span>
<span data-ttu-id="479fb-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="479fb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="479fb-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="479fb-113">-Name</span></span>
<span data-ttu-id="479fb-114">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="479fb-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="479fb-115">Il cmdlet Set-AzVMDscExtension imposta questo nome su Microsoft. PowerShell. DSC, che è lo stesso valore usato da **Get-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="479fb-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="479fb-116">Specifica questo parametro solo se il nome predefinito è stato modificato nel cmdlet **set-AzVMDscExtension** o si usa un nome di risorsa diverso in un modello di gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="479fb-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="479fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="479fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="479fb-118">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="479fb-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="479fb-119">-Stato</span><span class="sxs-lookup"><span data-stu-id="479fb-119">-Status</span></span>
<span data-ttu-id="479fb-120">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="479fb-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="479fb-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="479fb-121">-VMName</span></span>
<span data-ttu-id="479fb-122">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene l'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="479fb-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="479fb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="479fb-123">CommonParameters</span></span>
<span data-ttu-id="479fb-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="479fb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="479fb-125">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="479fb-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="479fb-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="479fb-126">INPUTS</span></span>

### <span data-ttu-id="479fb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="479fb-127">System.String</span></span>

### <span data-ttu-id="479fb-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="479fb-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="479fb-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="479fb-129">OUTPUTS</span></span>

### <span data-ttu-id="479fb-130">Microsoft. Azure. Commands. Compute. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="479fb-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="479fb-131">Note</span><span class="sxs-lookup"><span data-stu-id="479fb-131">NOTES</span></span>

## <span data-ttu-id="479fb-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="479fb-132">RELATED LINKS</span></span>

[<span data-ttu-id="479fb-133">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="479fb-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="479fb-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="479fb-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


