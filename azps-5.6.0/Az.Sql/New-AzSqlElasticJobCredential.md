---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 8f82162b0f1e5b1f43852880c77d1be1427e3ca1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970254"
---
# <span data-ttu-id="61ead-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="61ead-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="61ead-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61ead-102">SYNOPSIS</span></span>
<span data-ttu-id="61ead-103">Crea nuove credenziali di processo</span><span class="sxs-lookup"><span data-stu-id="61ead-103">Creates a new job credential</span></span>

## <span data-ttu-id="61ead-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61ead-104">SYNTAX</span></span>

### <span data-ttu-id="61ead-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61ead-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61ead-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="61ead-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61ead-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="61ead-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61ead-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="61ead-108">DESCRIPTION</span></span>
<span data-ttu-id="61ead-109">Il cmdlet New-AzSqlElasticJobCredential crea una nuova credenziali di processo</span><span class="sxs-lookup"><span data-stu-id="61ead-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="61ead-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61ead-110">EXAMPLES</span></span>

### <span data-ttu-id="61ead-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61ead-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="61ead-112">Crea nuove credenziali di processo</span><span class="sxs-lookup"><span data-stu-id="61ead-112">Creates a new job credential</span></span>

## <span data-ttu-id="61ead-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61ead-113">PARAMETERS</span></span>

### <span data-ttu-id="61ead-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="61ead-114">-AgentName</span></span>
<span data-ttu-id="61ead-115">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="61ead-115">The agent name</span></span>

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

### <span data-ttu-id="61ead-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="61ead-116">-Credential</span></span>
<span data-ttu-id="61ead-117">Credenziali</span><span class="sxs-lookup"><span data-stu-id="61ead-117">The credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ead-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ead-118">-DefaultProfile</span></span>
<span data-ttu-id="61ead-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61ead-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61ead-120">-Name</span><span class="sxs-lookup"><span data-stu-id="61ead-120">-Name</span></span>
<span data-ttu-id="61ead-121">Nome delle credenziali del processo</span><span class="sxs-lookup"><span data-stu-id="61ead-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ead-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="61ead-122">-ParentObject</span></span>
<span data-ttu-id="61ead-123">Oggetto agente</span><span class="sxs-lookup"><span data-stu-id="61ead-123">The agent object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61ead-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="61ead-124">-ParentResourceId</span></span>
<span data-ttu-id="61ead-125">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="61ead-125">The agent resource id</span></span>

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

### <span data-ttu-id="61ead-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61ead-126">-ResourceGroupName</span></span>
<span data-ttu-id="61ead-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="61ead-127">The resource group name</span></span>

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

### <span data-ttu-id="61ead-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="61ead-128">-ServerName</span></span>
<span data-ttu-id="61ead-129">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="61ead-129">The server name</span></span>

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

### <span data-ttu-id="61ead-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61ead-130">-Confirm</span></span>
<span data-ttu-id="61ead-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61ead-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61ead-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61ead-132">-WhatIf</span></span>
<span data-ttu-id="61ead-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61ead-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61ead-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61ead-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61ead-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ead-135">CommonParameters</span></span>
<span data-ttu-id="61ead-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61ead-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ead-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61ead-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ead-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="61ead-138">INPUTS</span></span>

### <span data-ttu-id="61ead-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="61ead-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="61ead-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="61ead-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="61ead-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61ead-141">OUTPUTS</span></span>

### <span data-ttu-id="61ead-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="61ead-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="61ead-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="61ead-143">NOTES</span></span>

## <span data-ttu-id="61ead-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61ead-144">RELATED LINKS</span></span>
