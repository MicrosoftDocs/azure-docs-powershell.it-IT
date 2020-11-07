---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: e9047b681e669975e7113eb3970b2ee6573a68d5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866131"
---
# <span data-ttu-id="505dd-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="505dd-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="505dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="505dd-102">SYNOPSIS</span></span>
<span data-ttu-id="505dd-103">Ottiene informazioni su un'estensione di chef.</span><span class="sxs-lookup"><span data-stu-id="505dd-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="505dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="505dd-104">SYNTAX</span></span>

### <span data-ttu-id="505dd-105">Linux</span><span class="sxs-lookup"><span data-stu-id="505dd-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="505dd-106">Windows</span><span class="sxs-lookup"><span data-stu-id="505dd-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="505dd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="505dd-107">DESCRIPTION</span></span>
<span data-ttu-id="505dd-108">Il cmdlet **Get-AzureVMChefExtension** ottiene le informazioni su un'estensione di chef installata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="505dd-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="505dd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="505dd-109">EXAMPLES</span></span>

### <span data-ttu-id="505dd-110">Esempio 1: ottenere i dettagli dell'estensione dello chef per una macchina virtuale di Windows-</span><span class="sxs-lookup"><span data-stu-id="505dd-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="505dd-111">Questo comando consente di ottenere l'estensione chef da una macchina virtuale di Windows denominata WindowsVM001 che appartiene al gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="505dd-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="505dd-112">Esempio 2: ottenere i dettagli dell'estensione dello chef per una macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="505dd-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="505dd-113">Questo comando consente di ottenere l'estensione dello chef da una macchina virtuale di Linux denominata LinuxVM001 che appartiene al gruppo di risorse denominato ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="505dd-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="505dd-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="505dd-114">PARAMETERS</span></span>

### <span data-ttu-id="505dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="505dd-115">-DefaultProfile</span></span>
<span data-ttu-id="505dd-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="505dd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="505dd-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="505dd-117">-Linux</span></span>
<span data-ttu-id="505dd-118">Indica che questo cmdlet funziona in una macchina virtuale Linux.</span><span class="sxs-lookup"><span data-stu-id="505dd-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505dd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="505dd-119">-Name</span></span>
<span data-ttu-id="505dd-120">Specifica il nome dell'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="505dd-120">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505dd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="505dd-121">-ResourceGroupName</span></span>
<span data-ttu-id="505dd-122">Specifica il nome del gruppo di risorse che contiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="505dd-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="505dd-123">-Stato</span><span class="sxs-lookup"><span data-stu-id="505dd-123">-Status</span></span>
<span data-ttu-id="505dd-124">Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza dell'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="505dd-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505dd-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="505dd-125">-VMName</span></span>
<span data-ttu-id="505dd-126">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="505dd-126">Specifies the name of a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505dd-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="505dd-127">-Windows</span></span>
<span data-ttu-id="505dd-128">Indica che questo cmdlet è per una macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="505dd-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="505dd-129">CommonParameters</span></span>
<span data-ttu-id="505dd-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="505dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="505dd-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="505dd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="505dd-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="505dd-132">INPUTS</span></span>

### <span data-ttu-id="505dd-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="505dd-133">None</span></span>
<span data-ttu-id="505dd-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="505dd-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="505dd-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="505dd-135">OUTPUTS</span></span>

### <span data-ttu-id="505dd-136">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="505dd-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="505dd-137">Note</span><span class="sxs-lookup"><span data-stu-id="505dd-137">NOTES</span></span>

## <span data-ttu-id="505dd-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="505dd-138">RELATED LINKS</span></span>

[<span data-ttu-id="505dd-139">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="505dd-139">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="505dd-140">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="505dd-140">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


