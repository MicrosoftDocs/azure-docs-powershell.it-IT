---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 5f5dac2f2028de9b90941ef91c38361c4357fc8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968237"
---
# <span data-ttu-id="27b62-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="27b62-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="27b62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27b62-102">SYNOPSIS</span></span>
<span data-ttu-id="27b62-103">Riprendere/risincronizzare la connessione nel volume di destinazione.</span><span class="sxs-lookup"><span data-stu-id="27b62-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="27b62-104">Se l'operazione viene eseguita nel volume di origine, la connessione viene risincronizzare la connessione e la sincronizzazione da origine a destinazione.</span><span class="sxs-lookup"><span data-stu-id="27b62-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="27b62-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27b62-105">SYNTAX</span></span>

### <span data-ttu-id="27b62-106">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27b62-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27b62-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27b62-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27b62-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27b62-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27b62-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="27b62-109">DESCRIPTION</span></span>
<span data-ttu-id="27b62-110">Riprendere/risincronizzare la connessione nel volume di destinazione</span><span class="sxs-lookup"><span data-stu-id="27b62-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="27b62-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27b62-111">EXAMPLES</span></span>

### <span data-ttu-id="27b62-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="27b62-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="27b62-113">Questo comando riprende la connessione a Replica ANF sul volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="27b62-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="27b62-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27b62-114">PARAMETERS</span></span>

### <span data-ttu-id="27b62-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="27b62-115">-AccountName</span></span>
<span data-ttu-id="27b62-116">Nome dell'account ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="27b62-116">The name of the ANF account of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b62-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b62-117">-DefaultProfile</span></span>
<span data-ttu-id="27b62-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27b62-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27b62-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27b62-119">-InputObject</span></span>
<span data-ttu-id="27b62-120">Oggetto volume di destinazione della replica ANF da risincronizzare</span><span class="sxs-lookup"><span data-stu-id="27b62-120">The ANF replication destination volume object to resync</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27b62-121">-Name</span><span class="sxs-lookup"><span data-stu-id="27b62-121">-Name</span></span>
<span data-ttu-id="27b62-122">Nome del volume di destinazione della replica ANF</span><span class="sxs-lookup"><span data-stu-id="27b62-122">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b62-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27b62-123">-PassThru</span></span>
<span data-ttu-id="27b62-124">Restituisce se è stata eseguita la sincronizzazione del volume di replica specificato</span><span class="sxs-lookup"><span data-stu-id="27b62-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="27b62-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="27b62-125">-PoolName</span></span>
<span data-ttu-id="27b62-126">Nome del pool ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="27b62-126">The name of the ANF pool of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b62-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27b62-127">-ResourceGroupName</span></span>
<span data-ttu-id="27b62-128">Gruppo di risorse del volume di destinazione della replica ANF</span><span class="sxs-lookup"><span data-stu-id="27b62-128">The resource group of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b62-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27b62-129">-ResourceId</span></span>
<span data-ttu-id="27b62-130">ID risorsa del volume di destinazione della replica ANF</span><span class="sxs-lookup"><span data-stu-id="27b62-130">The resource id of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b62-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27b62-131">-Confirm</span></span>
<span data-ttu-id="27b62-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27b62-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27b62-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27b62-133">-WhatIf</span></span>
<span data-ttu-id="27b62-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27b62-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27b62-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27b62-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27b62-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b62-136">CommonParameters</span></span>
<span data-ttu-id="27b62-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27b62-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b62-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="27b62-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b62-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="27b62-139">INPUTS</span></span>

### <span data-ttu-id="27b62-140">System.String</span><span class="sxs-lookup"><span data-stu-id="27b62-140">System.String</span></span>

### <span data-ttu-id="27b62-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="27b62-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="27b62-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27b62-142">OUTPUTS</span></span>

### <span data-ttu-id="27b62-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="27b62-143">System.Boolean</span></span>

## <span data-ttu-id="27b62-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="27b62-144">NOTES</span></span>

## <span data-ttu-id="27b62-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27b62-145">RELATED LINKS</span></span>
