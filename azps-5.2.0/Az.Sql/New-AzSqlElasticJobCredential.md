---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367188"
---
# <span data-ttu-id="3b3da-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="3b3da-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="3b3da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b3da-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3da-103">Crea una nuova credenziale processo</span><span class="sxs-lookup"><span data-stu-id="3b3da-103">Creates a new job credential</span></span>

## <span data-ttu-id="3b3da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b3da-104">SYNTAX</span></span>

### <span data-ttu-id="3b3da-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b3da-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b3da-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="3b3da-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b3da-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3b3da-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b3da-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b3da-108">DESCRIPTION</span></span>
<span data-ttu-id="3b3da-109">Il cmdlet New-AzSqlElasticJobCredential crea una nuova credenziale processo</span><span class="sxs-lookup"><span data-stu-id="3b3da-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="3b3da-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b3da-110">EXAMPLES</span></span>

### <span data-ttu-id="3b3da-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3b3da-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="3b3da-112">Crea una nuova credenziale processo</span><span class="sxs-lookup"><span data-stu-id="3b3da-112">Creates a new job credential</span></span>

## <span data-ttu-id="3b3da-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b3da-113">PARAMETERS</span></span>

### <span data-ttu-id="3b3da-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="3b3da-114">-AgentName</span></span>
<span data-ttu-id="3b3da-115">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="3b3da-115">The agent name</span></span>

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

### <span data-ttu-id="3b3da-116">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="3b3da-116">-Credential</span></span>
<span data-ttu-id="3b3da-117">Le credenziali</span><span class="sxs-lookup"><span data-stu-id="3b3da-117">The credential</span></span>

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

### <span data-ttu-id="3b3da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3da-118">-DefaultProfile</span></span>
<span data-ttu-id="3b3da-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b3da-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b3da-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b3da-120">-Name</span></span>
<span data-ttu-id="3b3da-121">Nome della credenziale processo</span><span class="sxs-lookup"><span data-stu-id="3b3da-121">The job credential name</span></span>

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

### <span data-ttu-id="3b3da-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3b3da-122">-ParentObject</span></span>
<span data-ttu-id="3b3da-123">Oggetto Agent</span><span class="sxs-lookup"><span data-stu-id="3b3da-123">The agent object</span></span>

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

### <span data-ttu-id="3b3da-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3b3da-124">-ParentResourceId</span></span>
<span data-ttu-id="3b3da-125">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="3b3da-125">The agent resource id</span></span>

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

### <span data-ttu-id="3b3da-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b3da-126">-ResourceGroupName</span></span>
<span data-ttu-id="3b3da-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3b3da-127">The resource group name</span></span>

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

### <span data-ttu-id="3b3da-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="3b3da-128">-ServerName</span></span>
<span data-ttu-id="3b3da-129">Nome del server</span><span class="sxs-lookup"><span data-stu-id="3b3da-129">The server name</span></span>

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

### <span data-ttu-id="3b3da-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3b3da-130">-Confirm</span></span>
<span data-ttu-id="3b3da-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b3da-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b3da-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b3da-132">-WhatIf</span></span>
<span data-ttu-id="3b3da-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b3da-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b3da-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b3da-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b3da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3da-135">CommonParameters</span></span>
<span data-ttu-id="3b3da-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3da-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b3da-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3da-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b3da-138">INPUTS</span></span>

### <span data-ttu-id="3b3da-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="3b3da-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="3b3da-140">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="3b3da-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="3b3da-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b3da-141">OUTPUTS</span></span>

### <span data-ttu-id="3b3da-142">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="3b3da-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="3b3da-143">Note</span><span class="sxs-lookup"><span data-stu-id="3b3da-143">NOTES</span></span>

## <span data-ttu-id="3b3da-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b3da-144">RELATED LINKS</span></span>
