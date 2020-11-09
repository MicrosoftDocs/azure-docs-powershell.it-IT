---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300463"
---
# <span data-ttu-id="6020b-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="6020b-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="6020b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6020b-102">SYNOPSIS</span></span>
<span data-ttu-id="6020b-103">Aggiorna le credenziali di un processo</span><span class="sxs-lookup"><span data-stu-id="6020b-103">Updates a job credential</span></span>

## <span data-ttu-id="6020b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6020b-104">SYNTAX</span></span>

### <span data-ttu-id="6020b-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6020b-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6020b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="6020b-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6020b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6020b-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6020b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6020b-108">DESCRIPTION</span></span>
<span data-ttu-id="6020b-109">Il cmdlet Set-AzSqlElasticJobCredential aggiorna le credenziali di un processo</span><span class="sxs-lookup"><span data-stu-id="6020b-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="6020b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6020b-110">EXAMPLES</span></span>

### <span data-ttu-id="6020b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6020b-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="6020b-112">Aggiorna le credenziali di un processo</span><span class="sxs-lookup"><span data-stu-id="6020b-112">Updates a job credential</span></span>

## <span data-ttu-id="6020b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6020b-113">PARAMETERS</span></span>

### <span data-ttu-id="6020b-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6020b-114">-AgentName</span></span>
<span data-ttu-id="6020b-115">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="6020b-115">The agent name</span></span>

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

### <span data-ttu-id="6020b-116">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="6020b-116">-Credential</span></span>
<span data-ttu-id="6020b-117">Le credenziali</span><span class="sxs-lookup"><span data-stu-id="6020b-117">The credential</span></span>

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

### <span data-ttu-id="6020b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6020b-118">-DefaultProfile</span></span>
<span data-ttu-id="6020b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6020b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6020b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6020b-120">-InputObject</span></span>
<span data-ttu-id="6020b-121">Oggetto credenziali processo</span><span class="sxs-lookup"><span data-stu-id="6020b-121">The job credential object</span></span>

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

### <span data-ttu-id="6020b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6020b-122">-Name</span></span>
<span data-ttu-id="6020b-123">Nome della credenziale processo</span><span class="sxs-lookup"><span data-stu-id="6020b-123">The job credential name</span></span>

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

### <span data-ttu-id="6020b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6020b-124">-ResourceGroupName</span></span>
<span data-ttu-id="6020b-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6020b-125">The resource group name</span></span>

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

### <span data-ttu-id="6020b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6020b-126">-ResourceId</span></span>
<span data-ttu-id="6020b-127">ID risorsa delle credenziali processo</span><span class="sxs-lookup"><span data-stu-id="6020b-127">The job credential resource id</span></span>

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

### <span data-ttu-id="6020b-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6020b-128">-ServerName</span></span>
<span data-ttu-id="6020b-129">Nome del server</span><span class="sxs-lookup"><span data-stu-id="6020b-129">The server name</span></span>

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

### <span data-ttu-id="6020b-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6020b-130">-Confirm</span></span>
<span data-ttu-id="6020b-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6020b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6020b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6020b-132">-WhatIf</span></span>
<span data-ttu-id="6020b-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6020b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6020b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6020b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6020b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6020b-135">CommonParameters</span></span>
<span data-ttu-id="6020b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6020b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6020b-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6020b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6020b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6020b-138">INPUTS</span></span>

### <span data-ttu-id="6020b-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="6020b-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="6020b-140">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="6020b-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="6020b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6020b-141">OUTPUTS</span></span>

### <span data-ttu-id="6020b-142">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="6020b-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="6020b-143">Note</span><span class="sxs-lookup"><span data-stu-id="6020b-143">NOTES</span></span>

## <span data-ttu-id="6020b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6020b-144">RELATED LINKS</span></span>
