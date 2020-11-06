---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
ms.openlocfilehash: 0a3c54331b557b6be279ab5ce3f9fafad62b158c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510023"
---
# <span data-ttu-id="0e9fc-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="0e9fc-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="0e9fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e9fc-102">SYNOPSIS</span></span>
<span data-ttu-id="0e9fc-103">Ottiene le impostazioni dell'estensione DSC in una particolare macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e9fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e9fc-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="0e9fc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e9fc-105">DESCRIPTION</span></span>
<span data-ttu-id="0e9fc-106">Il cmdlet **Get-AzureRmVMDscExtension** ottiene le impostazioni dell'estensione di configurazione dello stato desiderata in una determinata macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="0e9fc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e9fc-107">EXAMPLES</span></span>

### <span data-ttu-id="0e9fc-108">Esempio 1: ottenere le impostazioni di un'estensione DSC</span><span class="sxs-lookup"><span data-stu-id="0e9fc-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="0e9fc-109">Questo comando consente di ottenere le impostazioni di estensione denominate DSC nella macchina virtuale denominata VM07.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="0e9fc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e9fc-110">PARAMETERS</span></span>

### <span data-ttu-id="0e9fc-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e9fc-111">-Name</span></span>
<span data-ttu-id="0e9fc-112">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-112">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="0e9fc-113">Il cmdlet Set-AzureRmVMDscExtension imposta questo nome su Microsoft. PowerShell. DSC, che è lo stesso valore usato da **Get-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-113">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="0e9fc-114">Specifica questo parametro solo se il nome predefinito è stato modificato nel cmdlet **set-AzureRmVMDscExtension** o si usa un nome di risorsa diverso in un modello di gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-114">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="0e9fc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e9fc-115">-ResourceGroupName</span></span>
<span data-ttu-id="0e9fc-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0e9fc-117">-Stato</span><span class="sxs-lookup"><span data-stu-id="0e9fc-117">-Status</span></span>
<span data-ttu-id="0e9fc-118">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-118">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e9fc-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="0e9fc-119">-VMName</span></span>
<span data-ttu-id="0e9fc-120">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene l'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="0e9fc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e9fc-121">CommonParameters</span></span>
<span data-ttu-id="0e9fc-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e9fc-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e9fc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e9fc-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e9fc-124">INPUTS</span></span>

### <span data-ttu-id="0e9fc-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0e9fc-125">None</span></span>
<span data-ttu-id="0e9fc-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e9fc-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e9fc-127">OUTPUTS</span></span>

### <span data-ttu-id="0e9fc-128">Microsoft. Azure. Commands. Compute. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="0e9fc-128">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="0e9fc-129">Note</span><span class="sxs-lookup"><span data-stu-id="0e9fc-129">NOTES</span></span>

## <span data-ttu-id="0e9fc-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e9fc-130">RELATED LINKS</span></span>

[<span data-ttu-id="0e9fc-131">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="0e9fc-131">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="0e9fc-132">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="0e9fc-132">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


