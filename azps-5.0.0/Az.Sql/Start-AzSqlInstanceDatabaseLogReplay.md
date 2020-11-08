---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 61a87f61efaa889af830cc7bdaa44bcf0b7fc698
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193606"
---
# <span data-ttu-id="22278-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="22278-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="22278-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22278-102">SYNOPSIS</span></span>
<span data-ttu-id="22278-103">Avvia un servizio di riproduzione del log con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="22278-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="22278-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22278-104">SYNTAX</span></span>

### <span data-ttu-id="22278-105">LogReplayInstanceDatabaseFromInputParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22278-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22278-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="22278-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22278-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22278-107">DESCRIPTION</span></span>
<span data-ttu-id="22278-108">Il cmdlet **Start-AzSqlInstanceDatabaseLogReplay** avvia l'avvio del servizio di riproduzione del log.</span><span class="sxs-lookup"><span data-stu-id="22278-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="22278-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22278-109">EXAMPLES</span></span>

### <span data-ttu-id="22278-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22278-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="22278-111">Questo comando creerà un nuovo database gestito e inizierà a ripristinare i backup dal contenitore dato fino a quando non viene ripristinato last_backup. bak.</span><span class="sxs-lookup"><span data-stu-id="22278-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="22278-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="22278-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="22278-113">Questo comando creerà un nuovo database gestito e inizierà a ripristinare i backup dal contenitore dato fino a quando non viene chiamato Complete-AzSqlInstanceDatabaseLogReplay con l'ultimo backup desiderato.</span><span class="sxs-lookup"><span data-stu-id="22278-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="22278-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22278-114">PARAMETERS</span></span>

### <span data-ttu-id="22278-115">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="22278-115">-AutoCompleteRestore</span></span>
<span data-ttu-id="22278-116">L'indicatore se eseguire o meno il ripristino automatico al completamento.</span><span class="sxs-lookup"><span data-stu-id="22278-116">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="22278-117">-Regole di confronto</span><span class="sxs-lookup"><span data-stu-id="22278-117">-Collation</span></span>
<span data-ttu-id="22278-118">Regole di confronto del database dell'istanza da usare.</span><span class="sxs-lookup"><span data-stu-id="22278-118">The collation of the instance database to use.</span></span>

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

### <span data-ttu-id="22278-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22278-119">-DefaultProfile</span></span>
<span data-ttu-id="22278-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22278-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22278-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22278-121">-InputObject</span></span>
<span data-ttu-id="22278-122">Oggetto database dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="22278-122">The instance database object.</span></span>

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

### <span data-ttu-id="22278-123">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="22278-123">-InstanceName</span></span>
<span data-ttu-id="22278-124">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="22278-124">The name of the instance.</span></span>

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

### <span data-ttu-id="22278-125">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="22278-125">-LastBackupName</span></span>
<span data-ttu-id="22278-126">Nome dell'ultimo file di backup da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="22278-126">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="22278-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="22278-127">-Name</span></span>
<span data-ttu-id="22278-128">Nome del database dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="22278-128">The name of the instance database.</span></span>

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

### <span data-ttu-id="22278-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22278-129">-PassThru</span></span>
<span data-ttu-id="22278-130">Definisce se restituire il gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="22278-130">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="22278-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22278-131">-ResourceGroupName</span></span>
<span data-ttu-id="22278-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="22278-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="22278-133">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="22278-133">-StorageContainerSasToken</span></span>
<span data-ttu-id="22278-134">Token SAS del contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="22278-134">The storage container Sas token.</span></span>

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

### <span data-ttu-id="22278-135">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="22278-135">-StorageContainerUri</span></span>
<span data-ttu-id="22278-136">URI del contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="22278-136">The storage container URI.</span></span>

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

### <span data-ttu-id="22278-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="22278-137">-Confirm</span></span>
<span data-ttu-id="22278-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22278-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22278-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22278-139">-WhatIf</span></span>
<span data-ttu-id="22278-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22278-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22278-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22278-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22278-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22278-142">CommonParameters</span></span>
<span data-ttu-id="22278-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22278-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22278-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22278-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22278-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22278-145">INPUTS</span></span>

### <span data-ttu-id="22278-146">System. String</span><span class="sxs-lookup"><span data-stu-id="22278-146">System.String</span></span>

### <span data-ttu-id="22278-147">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="22278-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="22278-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22278-148">OUTPUTS</span></span>

### <span data-ttu-id="22278-149">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="22278-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="22278-150">Note</span><span class="sxs-lookup"><span data-stu-id="22278-150">NOTES</span></span>

## <span data-ttu-id="22278-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22278-151">RELATED LINKS</span></span>
