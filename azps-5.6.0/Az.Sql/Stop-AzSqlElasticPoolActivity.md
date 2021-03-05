---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: dbd0c93aca3750af846aa75ed369743fce5722ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008430"
---
# <span data-ttu-id="20b5e-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="20b5e-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="20b5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="20b5e-103">Annulla l'operazione di aggiornamento asincrono in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="20b5e-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="20b5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20b5e-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20b5e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="20b5e-105">DESCRIPTION</span></span>
<span data-ttu-id="20b5e-106">Il cmdlet **Stop-AzSqlElasticPoolActivity** annulla l'operazione di aggiornamento asincrono in un pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="20b5e-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="20b5e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20b5e-107">EXAMPLES</span></span>

### <span data-ttu-id="20b5e-108">Esempio 1: Annullare l'operazione di aggiornamento asincrono in un pool elastico</span><span class="sxs-lookup"><span data-stu-id="20b5e-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete :
```

<span data-ttu-id="20b5e-109">Questo comando annulla l'operazione di aggiornamento asincrono nel pool elastico.</span><span class="sxs-lookup"><span data-stu-id="20b5e-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="20b5e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20b5e-110">PARAMETERS</span></span>

### <span data-ttu-id="20b5e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b5e-111">-DefaultProfile</span></span>
<span data-ttu-id="20b5e-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20b5e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20b5e-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="20b5e-113">-ElasticPoolName</span></span>
<span data-ttu-id="20b5e-114">Nome del pool SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="20b5e-114">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20b5e-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="20b5e-115">-OperationId</span></span>
<span data-ttu-id="20b5e-116">ID dell'operazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="20b5e-116">The ID of the operation to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20b5e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20b5e-117">-PassThru</span></span>
<span data-ttu-id="20b5e-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="20b5e-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="20b5e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20b5e-119">-ResourceGroupName</span></span>
<span data-ttu-id="20b5e-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="20b5e-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="20b5e-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="20b5e-121">-ServerName</span></span>
<span data-ttu-id="20b5e-122">Il nome del gruppo di SQL Server Azure in cui si trova il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="20b5e-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="20b5e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20b5e-123">-Confirm</span></span>
<span data-ttu-id="20b5e-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20b5e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20b5e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b5e-125">-WhatIf</span></span>
<span data-ttu-id="20b5e-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20b5e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20b5e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20b5e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20b5e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b5e-128">CommonParameters</span></span>
<span data-ttu-id="20b5e-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20b5e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b5e-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="20b5e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b5e-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="20b5e-131">INPUTS</span></span>

### <span data-ttu-id="20b5e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="20b5e-132">System.String</span></span>

### <span data-ttu-id="20b5e-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="20b5e-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="20b5e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20b5e-134">OUTPUTS</span></span>

### <span data-ttu-id="20b5e-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="20b5e-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="20b5e-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="20b5e-136">NOTES</span></span>

## <span data-ttu-id="20b5e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20b5e-137">RELATED LINKS</span></span>
