---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextension
schema: 2.0.0
ms.openlocfilehash: 0954bcb395cf4a0dcf64dac178b1168ee1abd59b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866386"
---
# <span data-ttu-id="bd564-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="bd564-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="bd564-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd564-102">SYNOPSIS</span></span>
<span data-ttu-id="bd564-103">Ottiene le impostazioni dell'estensione DSC in una particolare macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bd564-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd564-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd564-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd564-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd564-105">DESCRIPTION</span></span>
<span data-ttu-id="bd564-106">Il cmdlet **Get-AzureRmVMDscExtension** ottiene le impostazioni dell'estensione di configurazione dello stato desiderata in una determinata macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bd564-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="bd564-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd564-107">EXAMPLES</span></span>

### <span data-ttu-id="bd564-108">Esempio 1: ottenere le impostazioni di un'estensione DSC</span><span class="sxs-lookup"><span data-stu-id="bd564-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="bd564-109">Questo comando consente di ottenere le impostazioni di estensione denominate DSC nella macchina virtuale denominata VM07.</span><span class="sxs-lookup"><span data-stu-id="bd564-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="bd564-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd564-110">PARAMETERS</span></span>

### <span data-ttu-id="bd564-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd564-111">-DefaultProfile</span></span>
<span data-ttu-id="bd564-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd564-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd564-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd564-113">-Name</span></span>
<span data-ttu-id="bd564-114">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="bd564-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="bd564-115">Il cmdlet Set-AzureRmVMDscExtension imposta questo nome su Microsoft. PowerShell. DSC, che è lo stesso valore usato da **Get-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="bd564-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="bd564-116">Specifica questo parametro solo se il nome predefinito è stato modificato nel cmdlet **set-AzureRmVMDscExtension** o si usa un nome di risorsa diverso in un modello di gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="bd564-116">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="bd564-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd564-117">-ResourceGroupName</span></span>
<span data-ttu-id="bd564-118">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bd564-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bd564-119">-Stato</span><span class="sxs-lookup"><span data-stu-id="bd564-119">-Status</span></span>
<span data-ttu-id="bd564-120">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="bd564-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="bd564-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="bd564-121">-VMName</span></span>
<span data-ttu-id="bd564-122">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene l'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="bd564-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="bd564-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd564-123">CommonParameters</span></span>
<span data-ttu-id="bd564-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd564-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd564-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd564-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd564-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd564-126">INPUTS</span></span>

### <span data-ttu-id="bd564-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd564-127">None</span></span>
<span data-ttu-id="bd564-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="bd564-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd564-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd564-129">OUTPUTS</span></span>

### <span data-ttu-id="bd564-130">Microsoft. Azure. Commands. Compute. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="bd564-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="bd564-131">Note</span><span class="sxs-lookup"><span data-stu-id="bd564-131">NOTES</span></span>

## <span data-ttu-id="bd564-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd564-132">RELATED LINKS</span></span>

[<span data-ttu-id="bd564-133">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="bd564-133">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="bd564-134">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="bd564-134">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


