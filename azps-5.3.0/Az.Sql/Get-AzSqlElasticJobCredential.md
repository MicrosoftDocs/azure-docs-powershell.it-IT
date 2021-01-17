---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1cd466581a89e49280d2a6cacdd74d4d37ac208d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376568"
---
# <span data-ttu-id="e85f3-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="e85f3-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="e85f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e85f3-102">SYNOPSIS</span></span>
<span data-ttu-id="e85f3-103">Ottiene una o più credenziali</span><span class="sxs-lookup"><span data-stu-id="e85f3-103">Gets one or more credentials</span></span>

## <span data-ttu-id="e85f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e85f3-104">SYNTAX</span></span>

### <span data-ttu-id="e85f3-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e85f3-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e85f3-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="e85f3-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e85f3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e85f3-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e85f3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e85f3-108">DESCRIPTION</span></span>
<span data-ttu-id="e85f3-109">Il cmdlet Get-AzSqlElasticJobCredential ottiene una o più credenziali del processo</span><span class="sxs-lookup"><span data-stu-id="e85f3-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="e85f3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e85f3-110">EXAMPLES</span></span>

### <span data-ttu-id="e85f3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e85f3-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="e85f3-112">Ottiene una credenziale processo</span><span class="sxs-lookup"><span data-stu-id="e85f3-112">Gets a job credential</span></span>

## <span data-ttu-id="e85f3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e85f3-113">PARAMETERS</span></span>

### <span data-ttu-id="e85f3-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e85f3-114">-AgentName</span></span>
<span data-ttu-id="e85f3-115">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="e85f3-115">The agent name</span></span>

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

### <span data-ttu-id="e85f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e85f3-116">-DefaultProfile</span></span>
<span data-ttu-id="e85f3-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e85f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e85f3-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e85f3-118">-Name</span></span>
<span data-ttu-id="e85f3-119">Nome della credenziale processo</span><span class="sxs-lookup"><span data-stu-id="e85f3-119">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e85f3-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e85f3-120">-ParentObject</span></span>
<span data-ttu-id="e85f3-121">Oggetto Agent</span><span class="sxs-lookup"><span data-stu-id="e85f3-121">The agent object</span></span>

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

### <span data-ttu-id="e85f3-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e85f3-122">-ParentResourceId</span></span>
<span data-ttu-id="e85f3-123">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="e85f3-123">The agent resource id</span></span>

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

### <span data-ttu-id="e85f3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e85f3-124">-ResourceGroupName</span></span>
<span data-ttu-id="e85f3-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e85f3-125">The resource group name</span></span>

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

### <span data-ttu-id="e85f3-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e85f3-126">-ServerName</span></span>
<span data-ttu-id="e85f3-127">Nome del server</span><span class="sxs-lookup"><span data-stu-id="e85f3-127">The server name</span></span>

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

### <span data-ttu-id="e85f3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e85f3-128">CommonParameters</span></span>
<span data-ttu-id="e85f3-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e85f3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e85f3-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e85f3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e85f3-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e85f3-131">INPUTS</span></span>

### <span data-ttu-id="e85f3-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="e85f3-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="e85f3-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e85f3-133">OUTPUTS</span></span>

### <span data-ttu-id="e85f3-134">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="e85f3-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="e85f3-135">Note</span><span class="sxs-lookup"><span data-stu-id="e85f3-135">NOTES</span></span>

## <span data-ttu-id="e85f3-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e85f3-136">RELATED LINKS</span></span>
