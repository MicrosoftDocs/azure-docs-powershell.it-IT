---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: 32f5973668ca03dedb22b05186eda83002167648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508619"
---
# <span data-ttu-id="9cac1-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9cac1-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="9cac1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9cac1-102">SYNOPSIS</span></span>
<span data-ttu-id="9cac1-103">Modifica le proprietà di diagnostica di avvio di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9cac1-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cac1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9cac1-104">SYNTAX</span></span>

### <span data-ttu-id="9cac1-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9cac1-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cac1-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9cac1-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cac1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cac1-107">DESCRIPTION</span></span>
<span data-ttu-id="9cac1-108">Il cmdlet **set-AzureRmVMBootDiagnostics** modifica le proprietà di diagnostica di avvio di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9cac1-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="9cac1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9cac1-109">EXAMPLES</span></span>

### <span data-ttu-id="9cac1-110">Esempio 1: abilitare la diagnostica di avvio</span><span class="sxs-lookup"><span data-stu-id="9cac1-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="9cac1-111">Il primo comando ottiene la macchina virtuale denominata ContosoVM07 tramite **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="9cac1-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="9cac1-112">Il comando lo archivia nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="9cac1-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="9cac1-113">Il secondo comando consente la diagnostica di avvio per la macchina virtuale in $VM.</span><span class="sxs-lookup"><span data-stu-id="9cac1-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="9cac1-114">I dati di diagnostica vengono archiviati nell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="9cac1-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="9cac1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9cac1-115">PARAMETERS</span></span>

### <span data-ttu-id="9cac1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cac1-116">-DefaultProfile</span></span>
<span data-ttu-id="9cac1-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9cac1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cac1-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="9cac1-118">-Disable</span></span>
<span data-ttu-id="9cac1-119">Indica che questo cmdlet disabilita la diagnostica di avvio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9cac1-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cac1-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="9cac1-120">-Enable</span></span>
<span data-ttu-id="9cac1-121">Indica che questo cmdlet Abilita la diagnostica di avvio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9cac1-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cac1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cac1-122">-ResourceGroupName</span></span>
<span data-ttu-id="9cac1-123">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9cac1-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cac1-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9cac1-124">-StorageAccountName</span></span>
<span data-ttu-id="9cac1-125">Specifica il nome dell'account di archiviazione in cui salvare i dati di diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="9cac1-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cac1-126">-VM</span><span class="sxs-lookup"><span data-stu-id="9cac1-126">-VM</span></span>
<span data-ttu-id="9cac1-127">Specifica la macchina virtuale per cui questo cmdlet modifica la diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="9cac1-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="9cac1-128">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="9cac1-128">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cac1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cac1-129">CommonParameters</span></span>
<span data-ttu-id="9cac1-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cac1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cac1-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cac1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cac1-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9cac1-132">INPUTS</span></span>

## <span data-ttu-id="9cac1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9cac1-133">OUTPUTS</span></span>

## <span data-ttu-id="9cac1-134">Note</span><span class="sxs-lookup"><span data-stu-id="9cac1-134">NOTES</span></span>

## <span data-ttu-id="9cac1-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9cac1-135">RELATED LINKS</span></span>

[<span data-ttu-id="9cac1-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cac1-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="9cac1-137">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="9cac1-137">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


