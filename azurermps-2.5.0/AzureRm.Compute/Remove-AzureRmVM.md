---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvm
schema: 2.0.0
ms.openlocfilehash: 5f816be5d3c024e43074d6a75c5ba79df4b2fdb3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866128"
---
# <span data-ttu-id="2d459-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d459-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="2d459-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d459-102">SYNOPSIS</span></span>
<span data-ttu-id="2d459-103">Rimuove una macchina virtuale da Azure.</span><span class="sxs-lookup"><span data-stu-id="2d459-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d459-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d459-104">SYNTAX</span></span>

### <span data-ttu-id="2d459-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2d459-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d459-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2d459-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d459-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d459-107">DESCRIPTION</span></span>
<span data-ttu-id="2d459-108">Il cmdlet **Remove-AzureRmVM** rimuove una macchina virtuale da Azure.</span><span class="sxs-lookup"><span data-stu-id="2d459-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="2d459-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d459-109">EXAMPLES</span></span>

### <span data-ttu-id="2d459-110">Esempio 1: rimuovere una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="2d459-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="2d459-111">Questo comando rimuove la macchina virtuale denominata VirtualMachine07 nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2d459-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="2d459-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d459-112">PARAMETERS</span></span>

### <span data-ttu-id="2d459-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d459-113">-AsJob</span></span>
<span data-ttu-id="2d459-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="2d459-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d459-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d459-115">-DefaultProfile</span></span>
<span data-ttu-id="2d459-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d459-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d459-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2d459-117">-Force</span></span>
<span data-ttu-id="2d459-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2d459-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d459-119">-ID</span><span class="sxs-lookup"><span data-stu-id="2d459-119">-Id</span></span>
<span data-ttu-id="2d459-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2d459-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d459-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d459-121">-Name</span></span>
<span data-ttu-id="2d459-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2d459-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d459-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d459-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d459-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2d459-124">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d459-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2d459-125">-Confirm</span></span>
<span data-ttu-id="2d459-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d459-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d459-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d459-127">-WhatIf</span></span>
<span data-ttu-id="2d459-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d459-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2d459-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d459-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d459-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d459-130">CommonParameters</span></span>
<span data-ttu-id="2d459-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d459-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d459-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d459-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d459-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d459-133">INPUTS</span></span>

### <span data-ttu-id="2d459-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2d459-134">None</span></span>
<span data-ttu-id="2d459-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2d459-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d459-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d459-136">OUTPUTS</span></span>

### <span data-ttu-id="2d459-137">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="2d459-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="2d459-138">Note</span><span class="sxs-lookup"><span data-stu-id="2d459-138">NOTES</span></span>

## <span data-ttu-id="2d459-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d459-139">RELATED LINKS</span></span>

[<span data-ttu-id="2d459-140">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d459-140">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="2d459-141">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d459-141">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="2d459-142">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d459-142">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="2d459-143">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d459-143">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="2d459-144">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d459-144">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="2d459-145">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d459-145">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


