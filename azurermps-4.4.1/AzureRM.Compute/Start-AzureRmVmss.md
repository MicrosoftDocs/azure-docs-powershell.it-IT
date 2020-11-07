---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 6b3291a77f7c69372124b8c0de2ba78c8810f02b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686590"
---
# <span data-ttu-id="7d903-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7d903-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="7d903-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d903-102">SYNOPSIS</span></span>
<span data-ttu-id="7d903-103">Avvia VMSS o un set di macchine virtuali all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="7d903-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d903-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d903-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d903-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d903-105">DESCRIPTION</span></span>
<span data-ttu-id="7d903-106">Il cmdlet **Start-AzureRmVmss** avvia tutte le macchine virtuali all'interno del set di scale della macchina virtuale (VMSS) o un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="7d903-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="7d903-107">Puoi usare il parametro *InstanceID* per selezionare un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="7d903-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="7d903-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d903-108">EXAMPLES</span></span>

### <span data-ttu-id="7d903-109">Esempio 1: avviare un set specifico di macchine virtuali all'interno di VMSS</span><span class="sxs-lookup"><span data-stu-id="7d903-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="7d903-110">Questo comando avvia un set specifico di macchine virtuali specificato dalla matrice di stringhe di ID istanza che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="7d903-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="7d903-111">Esempio 2: avviare tutte le macchine virtuali all'interno del VMSS</span><span class="sxs-lookup"><span data-stu-id="7d903-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="7d903-112">Questo comando avvia tutte le macchine virtuali che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="7d903-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="7d903-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d903-113">PARAMETERS</span></span>

### <span data-ttu-id="7d903-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d903-114">-DefaultProfile</span></span>
<span data-ttu-id="7d903-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d903-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d903-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="7d903-116">-InstanceId</span></span>
<span data-ttu-id="7d903-117">Specifica, come matrice di stringhe, l'ID o gli ID delle istanze avviate dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d903-117">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="7d903-118">Ad esempio: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="7d903-118">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d903-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d903-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d903-120">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="7d903-120">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="7d903-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7d903-121">-VMScaleSetName</span></span>
<span data-ttu-id="7d903-122">Specifica il nome del VMSS che questo cmdlet avvia le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="7d903-122">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d903-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d903-123">-Confirm</span></span>
<span data-ttu-id="7d903-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d903-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d903-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d903-125">-WhatIf</span></span>
<span data-ttu-id="7d903-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d903-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d903-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d903-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d903-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d903-128">CommonParameters</span></span>
<span data-ttu-id="7d903-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d903-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d903-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d903-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d903-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d903-131">INPUTS</span></span>

## <span data-ttu-id="7d903-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d903-132">OUTPUTS</span></span>

###  
<span data-ttu-id="7d903-133">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7d903-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="7d903-134">Note</span><span class="sxs-lookup"><span data-stu-id="7d903-134">NOTES</span></span>

## <span data-ttu-id="7d903-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d903-135">RELATED LINKS</span></span>

[<span data-ttu-id="7d903-136">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7d903-136">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="7d903-137">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7d903-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="7d903-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7d903-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="7d903-139">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7d903-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="7d903-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7d903-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="7d903-141">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7d903-141">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="7d903-142">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7d903-142">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


