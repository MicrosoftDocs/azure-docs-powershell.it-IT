---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: cd51835c2ca5a228e2eb3a54a4b3a724505e9d7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675109"
---
# <span data-ttu-id="27863-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="27863-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="27863-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27863-102">SYNOPSIS</span></span>
<span data-ttu-id="27863-103">Avvia un aggiornamento manuale dell'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="27863-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="27863-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27863-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27863-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27863-105">DESCRIPTION</span></span>
<span data-ttu-id="27863-106">Il cmdlet Update-AzVmssInstance avvia un aggiornamento manuale dell'istanza di VMSS (Virtual Machine scale set) specificata.</span><span class="sxs-lookup"><span data-stu-id="27863-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="27863-107">Viene usato quando il criterio di aggiornamento del set di scale VMSS è impostato su Manual.</span><span class="sxs-lookup"><span data-stu-id="27863-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="27863-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27863-108">EXAMPLES</span></span>

### <span data-ttu-id="27863-109">Esempio 1: avviare un aggiornamento dell'istanza di VMSS</span><span class="sxs-lookup"><span data-stu-id="27863-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="27863-110">Questo comando avvia un aggiornamento della VMSS denominata VMScaleSet001 che contiene l'ID istanza di 0.</span><span class="sxs-lookup"><span data-stu-id="27863-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="27863-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27863-111">PARAMETERS</span></span>

### <span data-ttu-id="27863-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27863-112">-AsJob</span></span>
<span data-ttu-id="27863-113">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="27863-113">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27863-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27863-114">-DefaultProfile</span></span>
<span data-ttu-id="27863-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27863-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27863-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="27863-116">-InstanceId</span></span>
<span data-ttu-id="27863-117">Specifica, come matrice di stringhe, l'ID o gli ID dell'istanza da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="27863-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27863-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27863-118">-ResourceGroupName</span></span>
<span data-ttu-id="27863-119">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="27863-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="27863-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="27863-120">-VMScaleSetName</span></span>
<span data-ttu-id="27863-121">Specifica il nome dell'istanza di VMSS che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="27863-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27863-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27863-122">-Confirm</span></span>
<span data-ttu-id="27863-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27863-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27863-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27863-124">-WhatIf</span></span>
<span data-ttu-id="27863-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27863-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27863-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27863-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27863-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27863-127">CommonParameters</span></span>
<span data-ttu-id="27863-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27863-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27863-129">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27863-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27863-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27863-130">INPUTS</span></span>

### <span data-ttu-id="27863-131">System. String</span><span class="sxs-lookup"><span data-stu-id="27863-131">System.String</span></span>

### <span data-ttu-id="27863-132">System. String []</span><span class="sxs-lookup"><span data-stu-id="27863-132">System.String[]</span></span>

## <span data-ttu-id="27863-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27863-133">OUTPUTS</span></span>

### <span data-ttu-id="27863-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="27863-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="27863-135">Note</span><span class="sxs-lookup"><span data-stu-id="27863-135">NOTES</span></span>

## <span data-ttu-id="27863-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27863-136">RELATED LINKS</span></span>

[<span data-ttu-id="27863-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27863-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


