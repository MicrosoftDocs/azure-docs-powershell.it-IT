---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: 5a848c2e4a13df6a38c67e067531ff8581bd595e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508659"
---
# <span data-ttu-id="b0a6c-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b0a6c-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="b0a6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a6c-103">Riavvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a6c-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0a6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0a6c-104">SYNTAX</span></span>

### <span data-ttu-id="b0a6c-105">RestartResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0a6c-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a6c-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b0a6c-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a6c-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b0a6c-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a6c-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b0a6c-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0a6c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0a6c-109">DESCRIPTION</span></span>
<span data-ttu-id="b0a6c-110">Il cmdlet **Restart-AzureRmVM riavvia** una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a6c-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="b0a6c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0a6c-111">EXAMPLES</span></span>

### <span data-ttu-id="b0a6c-112">Esempio 1: riavviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b0a6c-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b0a6c-113">Questo comando Riavvia la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b0a6c-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="b0a6c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0a6c-114">PARAMETERS</span></span>

### <span data-ttu-id="b0a6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a6c-115">-DefaultProfile</span></span>
<span data-ttu-id="b0a6c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a6c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0a6c-117">-ID</span><span class="sxs-lookup"><span data-stu-id="b0a6c-117">-Id</span></span>
<span data-ttu-id="b0a6c-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0a6c-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a6c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0a6c-119">-Name</span></span>
<span data-ttu-id="b0a6c-120">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b0a6c-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="b0a6c-121">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="b0a6c-121">-PerformMaintenance</span></span>
<span data-ttu-id="b0a6c-122">Per eseguire la manutenzione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b0a6c-122">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a6c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0a6c-123">-ResourceGroupName</span></span>
<span data-ttu-id="b0a6c-124">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b0a6c-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a6c-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0a6c-125">-Confirm</span></span>
<span data-ttu-id="b0a6c-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0a6c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0a6c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0a6c-127">-WhatIf</span></span>
<span data-ttu-id="b0a6c-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0a6c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0a6c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0a6c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0a6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a6c-130">CommonParameters</span></span>
<span data-ttu-id="b0a6c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0a6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a6c-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0a6c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a6c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0a6c-133">INPUTS</span></span>

## <span data-ttu-id="b0a6c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0a6c-134">OUTPUTS</span></span>

## <span data-ttu-id="b0a6c-135">Note</span><span class="sxs-lookup"><span data-stu-id="b0a6c-135">NOTES</span></span>

## <span data-ttu-id="b0a6c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0a6c-136">RELATED LINKS</span></span>

[<span data-ttu-id="b0a6c-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b0a6c-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b0a6c-138">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b0a6c-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="b0a6c-139">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b0a6c-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="b0a6c-140">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b0a6c-140">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="b0a6c-141">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b0a6c-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="b0a6c-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b0a6c-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


