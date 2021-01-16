---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354340"
---
# <span data-ttu-id="760f0-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="760f0-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="760f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="760f0-102">SYNOPSIS</span></span>
<span data-ttu-id="760f0-103">Riprendere/risincronizzare la connessione nel volume di destinazione.</span><span class="sxs-lookup"><span data-stu-id="760f0-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="760f0-104">Se l'operazione viene eseguita nel volume di origine, risincronizza la connessione e la sincronizza dall'origine alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="760f0-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="760f0-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="760f0-105">SYNTAX</span></span>

### <span data-ttu-id="760f0-106">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="760f0-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="760f0-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="760f0-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="760f0-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="760f0-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="760f0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="760f0-109">DESCRIPTION</span></span>
<span data-ttu-id="760f0-110">Riprendere/risincronizzare la connessione nel volume di destinazione</span><span class="sxs-lookup"><span data-stu-id="760f0-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="760f0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="760f0-111">EXAMPLES</span></span>

### <span data-ttu-id="760f0-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="760f0-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="760f0-113">Questo comando riprende la connessione di replica ANF nel volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="760f0-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="760f0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="760f0-114">PARAMETERS</span></span>

### <span data-ttu-id="760f0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="760f0-115">-AccountName</span></span>
<span data-ttu-id="760f0-116">Nome dell'account di ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="760f0-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="760f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="760f0-117">-DefaultProfile</span></span>
<span data-ttu-id="760f0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="760f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="760f0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="760f0-119">-InputObject</span></span>
<span data-ttu-id="760f0-120">Oggetto volume di destinazione della replica ANF da risincronizzare</span><span class="sxs-lookup"><span data-stu-id="760f0-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="760f0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="760f0-121">-Name</span></span>
<span data-ttu-id="760f0-122">Nome del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="760f0-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="760f0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="760f0-123">-PassThru</span></span>
<span data-ttu-id="760f0-124">Restituisce se è stata eseguita la risincronizzazione del volume di replica specificato</span><span class="sxs-lookup"><span data-stu-id="760f0-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="760f0-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="760f0-125">-PoolName</span></span>
<span data-ttu-id="760f0-126">Nome del pool di ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="760f0-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="760f0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="760f0-127">-ResourceGroupName</span></span>
<span data-ttu-id="760f0-128">Gruppo risorse del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="760f0-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="760f0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="760f0-129">-ResourceId</span></span>
<span data-ttu-id="760f0-130">ID risorsa del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="760f0-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="760f0-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="760f0-131">-Confirm</span></span>
<span data-ttu-id="760f0-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="760f0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="760f0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="760f0-133">-WhatIf</span></span>
<span data-ttu-id="760f0-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="760f0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="760f0-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="760f0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="760f0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="760f0-136">CommonParameters</span></span>
<span data-ttu-id="760f0-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="760f0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="760f0-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="760f0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="760f0-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="760f0-139">INPUTS</span></span>

### <span data-ttu-id="760f0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="760f0-140">System.String</span></span>

### <span data-ttu-id="760f0-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="760f0-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="760f0-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="760f0-142">OUTPUTS</span></span>

### <span data-ttu-id="760f0-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="760f0-143">System.Boolean</span></span>

## <span data-ttu-id="760f0-144">Note</span><span class="sxs-lookup"><span data-stu-id="760f0-144">NOTES</span></span>

## <span data-ttu-id="760f0-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="760f0-145">RELATED LINKS</span></span>
