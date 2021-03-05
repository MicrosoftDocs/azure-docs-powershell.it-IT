---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: ce937cc6f7e4bc68592ed089a3028e2919fde29f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963582"
---
# <span data-ttu-id="3cdfd-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="3cdfd-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="3cdfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cdfd-102">SYNOPSIS</span></span>
<span data-ttu-id="3cdfd-103">Avvia un servizio di riproduzione del log con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="3cdfd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3cdfd-104">SYNTAX</span></span>

### <span data-ttu-id="3cdfd-105">LogReplayInstanceDatabaseFromInputParameters (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3cdfd-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cdfd-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="3cdfd-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cdfd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3cdfd-107">DESCRIPTION</span></span>
<span data-ttu-id="3cdfd-108">Il cmdlet **Start-AzSqlInstanceDatabaseLogReplay** avvia l'avvio del servizio di riproduzione del log.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="3cdfd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3cdfd-109">EXAMPLES</span></span>

### <span data-ttu-id="3cdfd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3cdfd-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="3cdfd-111">Questo comando crea un nuovo database gestito e avvia il ripristino dei backup dal contenitore specificato finché last_backup il file bak non viene ripristinato.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="3cdfd-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3cdfd-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="3cdfd-113">Questo comando crea un nuovo database gestito e avvia il ripristino dei backup dal contenitore specificato finché Complete-AzSqlInstanceDatabaseLogReplay chiamata con l'ultimo backup desiderato.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="3cdfd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cdfd-114">PARAMETERS</span></span>

### <span data-ttu-id="3cdfd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cdfd-115">-AsJob</span></span>
<span data-ttu-id="3cdfd-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3cdfd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cdfd-117">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="3cdfd-117">-AutoCompleteRestore</span></span>
<span data-ttu-id="3cdfd-118">Indicatore che indica se eseguire o meno il ripristino automatico al completamento.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-118">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="3cdfd-119">-Collation</span><span class="sxs-lookup"><span data-stu-id="3cdfd-119">-Collation</span></span>
<span data-ttu-id="3cdfd-120">Fascicolazione del database delle istanze da usare.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-120">The collation of the instance database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cdfd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cdfd-121">-DefaultProfile</span></span>
<span data-ttu-id="3cdfd-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cdfd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cdfd-123">-InputObject</span></span>
<span data-ttu-id="3cdfd-124">Oggetto di database dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-124">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cdfd-125">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3cdfd-125">-InstanceName</span></span>
<span data-ttu-id="3cdfd-126">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-126">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cdfd-127">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="3cdfd-127">-LastBackupName</span></span>
<span data-ttu-id="3cdfd-128">Nome dell'ultimo file di backup da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-128">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cdfd-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3cdfd-129">-Name</span></span>
<span data-ttu-id="3cdfd-130">Nome del database dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-130">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cdfd-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cdfd-131">-PassThru</span></span>
<span data-ttu-id="3cdfd-132">Definisce se restituire il gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-132">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="3cdfd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cdfd-133">-ResourceGroupName</span></span>
<span data-ttu-id="3cdfd-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cdfd-135">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="3cdfd-135">-StorageContainerSasToken</span></span>
<span data-ttu-id="3cdfd-136">Token sas del contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-136">The storage container Sas token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasToken

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cdfd-137">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="3cdfd-137">-StorageContainerUri</span></span>
<span data-ttu-id="3cdfd-138">URI del contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-138">The storage container URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Storage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cdfd-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cdfd-139">-Confirm</span></span>
<span data-ttu-id="3cdfd-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cdfd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cdfd-141">-WhatIf</span></span>
<span data-ttu-id="3cdfd-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cdfd-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cdfd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cdfd-144">CommonParameters</span></span>
<span data-ttu-id="3cdfd-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cdfd-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cdfd-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="3cdfd-147">INPUTS</span></span>

### <span data-ttu-id="3cdfd-148">System.String</span><span class="sxs-lookup"><span data-stu-id="3cdfd-148">System.String</span></span>

### <span data-ttu-id="3cdfd-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3cdfd-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="3cdfd-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3cdfd-150">OUTPUTS</span></span>

### <span data-ttu-id="3cdfd-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3cdfd-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="3cdfd-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="3cdfd-152">NOTES</span></span>

## <span data-ttu-id="3cdfd-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3cdfd-153">RELATED LINKS</span></span>
