---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: e99e2e6a8c0b2c8a0fc0b2d2143d2b4301520ab0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952653"
---
# <span data-ttu-id="79737-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="79737-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="79737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79737-102">SYNOPSIS</span></span>
<span data-ttu-id="79737-103">Crea un nuovo comando da eseguire su un'attività DMS esistente.</span><span class="sxs-lookup"><span data-stu-id="79737-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="79737-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79737-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="79737-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79737-105">DESCRIPTION</span></span>
<span data-ttu-id="79737-106">Il Invoke-AzDataMigrationCommand cmdlet crea una nuova attività di comando da eseguire su un'attività di migrazione esistente.</span><span class="sxs-lookup"><span data-stu-id="79737-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="79737-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79737-107">EXAMPLES</span></span>

### <span data-ttu-id="79737-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79737-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="79737-109">Negli esempi precedenti viene utilizzato il cmdlet Invoke-AzDataMigrationCommand per creare un comando per un servizio, un progetto e un'attività esistenti</span><span class="sxs-lookup"><span data-stu-id="79737-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="79737-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79737-110">PARAMETERS</span></span>

### <span data-ttu-id="79737-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="79737-111">-CommandType</span></span>
<span data-ttu-id="79737-112">Tipo di comando.</span><span class="sxs-lookup"><span data-stu-id="79737-112">Command Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.CommandTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: CompleteSqlDBSync, CancelMongoDB, RestartMongoDB, FinishMongoDB, CompleteSqlMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79737-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79737-113">-DefaultProfile</span></span>
<span data-ttu-id="79737-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79737-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79737-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="79737-115">-ProjectName</span></span>
<span data-ttu-id="79737-116">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="79737-116">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79737-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79737-117">-ResourceGroupName</span></span>
<span data-ttu-id="79737-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="79737-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79737-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="79737-119">-ServiceName</span></span>
<span data-ttu-id="79737-120">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="79737-120">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79737-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="79737-121">-TaskName</span></span>
<span data-ttu-id="79737-122">Nome dell'attività su cui viene eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="79737-122">The name of the task the command is run on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="79737-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="79737-123">-ObjectName</span></span>
<span data-ttu-id="79737-124">Nome dell'oggetto di database su cui verrà eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="79737-124">The name of the database object the command will run against.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79737-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79737-125">-Confirm</span></span>
<span data-ttu-id="79737-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79737-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79737-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79737-127">-WhatIf</span></span>
<span data-ttu-id="79737-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79737-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79737-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79737-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79737-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79737-130">CommonParameters</span></span>
<span data-ttu-id="79737-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79737-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79737-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79737-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79737-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="79737-133">INPUTS</span></span>

### <span data-ttu-id="79737-134">System.String</span><span class="sxs-lookup"><span data-stu-id="79737-134">System.String</span></span>

## <span data-ttu-id="79737-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79737-135">OUTPUTS</span></span>

### <span data-ttu-id="79737-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span><span class="sxs-lookup"><span data-stu-id="79737-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="79737-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="79737-137">NOTES</span></span>

## <span data-ttu-id="79737-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79737-138">RELATED LINKS</span></span>
