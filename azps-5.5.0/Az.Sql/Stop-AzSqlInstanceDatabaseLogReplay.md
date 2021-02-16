---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209163"
---
# <span data-ttu-id="a8758-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="a8758-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="a8758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8758-102">SYNOPSIS</span></span>
<span data-ttu-id="a8758-103">Annulla il servizio di riproduzione del log eliminando il database.</span><span class="sxs-lookup"><span data-stu-id="a8758-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="a8758-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8758-104">SYNTAX</span></span>

### <span data-ttu-id="a8758-105">LogReplayInstanceDatabaseFromInputParameters (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8758-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8758-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="a8758-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8758-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a8758-107">DESCRIPTION</span></span>
<span data-ttu-id="a8758-108">Il cmdlet **Stop-AzSqlInstanceDatabaseLogReplay** elimina il database e quindi annulla il servizio di riproduzione del log.</span><span class="sxs-lookup"><span data-stu-id="a8758-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="a8758-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8758-109">EXAMPLES</span></span>

### <span data-ttu-id="a8758-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a8758-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="a8758-111">Questo comando annulla il servizio di riproduzione del log nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="a8758-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="a8758-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8758-112">PARAMETERS</span></span>

### <span data-ttu-id="a8758-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8758-113">-DefaultProfile</span></span>
<span data-ttu-id="a8758-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8758-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8758-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a8758-115">-Force</span></span>
<span data-ttu-id="a8758-116">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="a8758-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a8758-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8758-117">-InputObject</span></span>
<span data-ttu-id="a8758-118">Oggetto di database dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a8758-118">The instance database object.</span></span>

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

### <span data-ttu-id="a8758-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a8758-119">-InstanceName</span></span>
<span data-ttu-id="a8758-120">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a8758-120">The name of the instance.</span></span>

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

### <span data-ttu-id="a8758-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a8758-121">-Name</span></span>
<span data-ttu-id="a8758-122">Nome del database dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a8758-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="a8758-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8758-123">-PassThru</span></span>
<span data-ttu-id="a8758-124">Definisce se restituire il gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="a8758-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="a8758-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8758-125">-ResourceGroupName</span></span>
<span data-ttu-id="a8758-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a8758-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="a8758-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8758-127">-Confirm</span></span>
<span data-ttu-id="a8758-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8758-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8758-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8758-129">-WhatIf</span></span>
<span data-ttu-id="a8758-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8758-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8758-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8758-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8758-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8758-132">CommonParameters</span></span>
<span data-ttu-id="a8758-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8758-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8758-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a8758-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8758-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="a8758-135">INPUTS</span></span>

### <span data-ttu-id="a8758-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a8758-136">System.String</span></span>

### <span data-ttu-id="a8758-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a8758-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="a8758-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8758-138">OUTPUTS</span></span>

### <span data-ttu-id="a8758-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a8758-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="a8758-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="a8758-140">NOTES</span></span>

## <span data-ttu-id="a8758-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8758-141">RELATED LINKS</span></span>
