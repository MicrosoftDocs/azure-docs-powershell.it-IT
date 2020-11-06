---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
ms.openlocfilehash: 5733939c24437c974f629588106d6240766a9df1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514515"
---
# <span data-ttu-id="3934a-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3934a-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="3934a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3934a-102">SYNOPSIS</span></span>
<span data-ttu-id="3934a-103">Ottiene informazioni su un'estensione di chef.</span><span class="sxs-lookup"><span data-stu-id="3934a-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3934a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3934a-104">SYNTAX</span></span>

### <span data-ttu-id="3934a-105">Linux</span><span class="sxs-lookup"><span data-stu-id="3934a-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [<CommonParameters>]
```

### <span data-ttu-id="3934a-106">Windows</span><span class="sxs-lookup"><span data-stu-id="3934a-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [<CommonParameters>]
```

## <span data-ttu-id="3934a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3934a-107">DESCRIPTION</span></span>
<span data-ttu-id="3934a-108">Il cmdlet **Get-AzureVMChefExtension** ottiene le informazioni su un'estensione di chef installata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3934a-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="3934a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3934a-109">EXAMPLES</span></span>

### <span data-ttu-id="3934a-110">Esempio 1: ottenere i dettagli dell'estensione dello chef per una macchina virtuale di Windows-</span><span class="sxs-lookup"><span data-stu-id="3934a-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="3934a-111">Questo comando consente di ottenere l'estensione chef da una macchina virtuale di Windows denominata WindowsVM001 che appartiene al gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="3934a-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="3934a-112">Esempio 2: ottenere i dettagli dell'estensione dello chef per una macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="3934a-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="3934a-113">Questo comando consente di ottenere l'estensione dello chef da una macchina virtuale di Linux denominata LinuxVM001 che appartiene al gruppo di risorse denominato ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="3934a-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="3934a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3934a-114">PARAMETERS</span></span>

### <span data-ttu-id="3934a-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="3934a-115">-Linux</span></span>
<span data-ttu-id="3934a-116">Indica che questo cmdlet funziona in una macchina virtuale Linux.</span><span class="sxs-lookup"><span data-stu-id="3934a-116">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

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

### <span data-ttu-id="3934a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3934a-117">-Name</span></span>
<span data-ttu-id="3934a-118">Specifica il nome dell'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="3934a-118">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="3934a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3934a-119">-ResourceGroupName</span></span>
<span data-ttu-id="3934a-120">Specifica il nome del gruppo di risorse che contiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3934a-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="3934a-121">-Stato</span><span class="sxs-lookup"><span data-stu-id="3934a-121">-Status</span></span>
<span data-ttu-id="3934a-122">Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza dell'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="3934a-122">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="3934a-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="3934a-123">-VMName</span></span>
<span data-ttu-id="3934a-124">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3934a-124">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="3934a-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="3934a-125">-Windows</span></span>
<span data-ttu-id="3934a-126">Indica che questo cmdlet è per una macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="3934a-126">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

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

### <span data-ttu-id="3934a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3934a-127">CommonParameters</span></span>
<span data-ttu-id="3934a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3934a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3934a-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3934a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3934a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3934a-130">INPUTS</span></span>

### <span data-ttu-id="3934a-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3934a-131">None</span></span>
<span data-ttu-id="3934a-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3934a-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3934a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3934a-133">OUTPUTS</span></span>

## <span data-ttu-id="3934a-134">Note</span><span class="sxs-lookup"><span data-stu-id="3934a-134">NOTES</span></span>

## <span data-ttu-id="3934a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3934a-135">RELATED LINKS</span></span>

[<span data-ttu-id="3934a-136">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3934a-136">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="3934a-137">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3934a-137">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


