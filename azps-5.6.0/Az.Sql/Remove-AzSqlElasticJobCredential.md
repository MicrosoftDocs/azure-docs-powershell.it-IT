---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: d5ee112af595ba88672a26d0f8f64590ea670706
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961341"
---
# <span data-ttu-id="82f62-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="82f62-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="82f62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82f62-102">SYNOPSIS</span></span>
<span data-ttu-id="82f62-103">Rimuove le credenziali del processo flessibile</span><span class="sxs-lookup"><span data-stu-id="82f62-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="82f62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82f62-104">SYNTAX</span></span>

### <span data-ttu-id="82f62-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82f62-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82f62-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="82f62-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82f62-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="82f62-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82f62-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="82f62-108">DESCRIPTION</span></span>
<span data-ttu-id="82f62-109">Il cmdlet Remove-AzSqlElasticJobCredential rimuove le credenziali di un processo</span><span class="sxs-lookup"><span data-stu-id="82f62-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="82f62-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82f62-110">EXAMPLES</span></span>

### <span data-ttu-id="82f62-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82f62-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="82f62-112">Rimuove le credenziali di un processo</span><span class="sxs-lookup"><span data-stu-id="82f62-112">Removes a job credential</span></span>

## <span data-ttu-id="82f62-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82f62-113">PARAMETERS</span></span>

### <span data-ttu-id="82f62-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="82f62-114">-AgentName</span></span>
<span data-ttu-id="82f62-115">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="82f62-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f62-116">-DefaultProfile</span></span>
<span data-ttu-id="82f62-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82f62-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82f62-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82f62-118">-InputObject</span></span>
<span data-ttu-id="82f62-119">Oggetto credenziali processo</span><span class="sxs-lookup"><span data-stu-id="82f62-119">The job credential object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82f62-120">-Name</span><span class="sxs-lookup"><span data-stu-id="82f62-120">-Name</span></span>
<span data-ttu-id="82f62-121">Nome delle credenziali del processo</span><span class="sxs-lookup"><span data-stu-id="82f62-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f62-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82f62-122">-ResourceGroupName</span></span>
<span data-ttu-id="82f62-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="82f62-123">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f62-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82f62-124">-ResourceId</span></span>
<span data-ttu-id="82f62-125">ID risorsa credenziali processo</span><span class="sxs-lookup"><span data-stu-id="82f62-125">The job credential resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82f62-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="82f62-126">-ServerName</span></span>
<span data-ttu-id="82f62-127">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="82f62-127">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f62-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82f62-128">-Confirm</span></span>
<span data-ttu-id="82f62-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82f62-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82f62-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82f62-130">-WhatIf</span></span>
<span data-ttu-id="82f62-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82f62-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82f62-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82f62-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82f62-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f62-133">CommonParameters</span></span>
<span data-ttu-id="82f62-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82f62-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f62-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82f62-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f62-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="82f62-136">INPUTS</span></span>

### <span data-ttu-id="82f62-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="82f62-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="82f62-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82f62-138">OUTPUTS</span></span>

### <span data-ttu-id="82f62-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="82f62-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="82f62-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="82f62-140">NOTES</span></span>

## <span data-ttu-id="82f62-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82f62-141">RELATED LINKS</span></span>
