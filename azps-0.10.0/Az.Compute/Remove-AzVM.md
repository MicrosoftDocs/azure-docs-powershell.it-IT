---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 4cdf61c8a5afca78f1701314476d9eacb862cdfb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863557"
---
# <span data-ttu-id="bc7d0-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="bc7d0-101">Remove-AzVM</span></span>

## <span data-ttu-id="bc7d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc7d0-102">SYNOPSIS</span></span>
<span data-ttu-id="bc7d0-103">Rimuove una macchina virtuale da Azure.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="bc7d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc7d0-104">SYNTAX</span></span>

### <span data-ttu-id="bc7d0-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bc7d0-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc7d0-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bc7d0-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc7d0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc7d0-107">DESCRIPTION</span></span>
<span data-ttu-id="bc7d0-108">Il cmdlet **Remove-AzVM** rimuove una macchina virtuale da Azure.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="bc7d0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc7d0-109">EXAMPLES</span></span>

### <span data-ttu-id="bc7d0-110">Esempio 1: rimuovere una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="bc7d0-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="bc7d0-111">Questo comando rimuove la macchina virtuale denominata VirtualMachine07 nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="bc7d0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc7d0-112">PARAMETERS</span></span>

### <span data-ttu-id="bc7d0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc7d0-113">-AsJob</span></span>
<span data-ttu-id="bc7d0-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bc7d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc7d0-115">-DefaultProfile</span></span>
<span data-ttu-id="bc7d0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc7d0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bc7d0-117">-Force</span></span>
<span data-ttu-id="bc7d0-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc7d0-119">-ID</span><span class="sxs-lookup"><span data-stu-id="bc7d0-119">-Id</span></span>
<span data-ttu-id="bc7d0-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-120">The resource group name.</span></span>

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

### <span data-ttu-id="bc7d0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc7d0-121">-Name</span></span>
<span data-ttu-id="bc7d0-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-122">The resource name.</span></span>

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

### <span data-ttu-id="bc7d0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc7d0-123">-ResourceGroupName</span></span>
<span data-ttu-id="bc7d0-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bc7d0-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bc7d0-125">-Confirm</span></span>
<span data-ttu-id="bc7d0-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc7d0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc7d0-127">-WhatIf</span></span>
<span data-ttu-id="bc7d0-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="bc7d0-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc7d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc7d0-130">CommonParameters</span></span>
<span data-ttu-id="bc7d0-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc7d0-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc7d0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc7d0-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc7d0-133">INPUTS</span></span>

### <span data-ttu-id="bc7d0-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bc7d0-134">None</span></span>
<span data-ttu-id="bc7d0-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="bc7d0-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bc7d0-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc7d0-136">OUTPUTS</span></span>

### <span data-ttu-id="bc7d0-137">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="bc7d0-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="bc7d0-138">Note</span><span class="sxs-lookup"><span data-stu-id="bc7d0-138">NOTES</span></span>

## <span data-ttu-id="bc7d0-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc7d0-139">RELATED LINKS</span></span>

[<span data-ttu-id="bc7d0-140">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="bc7d0-140">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="bc7d0-141">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="bc7d0-141">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="bc7d0-142">Riavviare-AzVM</span><span class="sxs-lookup"><span data-stu-id="bc7d0-142">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="bc7d0-143">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="bc7d0-143">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="bc7d0-144">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="bc7d0-144">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="bc7d0-145">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bc7d0-145">Update-AzVM</span></span>](./Update-AzVM.md)


