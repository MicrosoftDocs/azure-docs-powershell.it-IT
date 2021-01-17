---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353620"
---
# <span data-ttu-id="233fb-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="233fb-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="233fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="233fb-102">SYNOPSIS</span></span>
<span data-ttu-id="233fb-103">Rimuove le credenziali per i processi elastici</span><span class="sxs-lookup"><span data-stu-id="233fb-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="233fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="233fb-104">SYNTAX</span></span>

### <span data-ttu-id="233fb-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="233fb-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="233fb-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="233fb-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="233fb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="233fb-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="233fb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="233fb-108">DESCRIPTION</span></span>
<span data-ttu-id="233fb-109">Il cmdlet Remove-AzSqlElasticJobCredential rimuove le credenziali di un processo</span><span class="sxs-lookup"><span data-stu-id="233fb-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="233fb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="233fb-110">EXAMPLES</span></span>

### <span data-ttu-id="233fb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="233fb-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="233fb-112">Rimuove le credenziali di un processo</span><span class="sxs-lookup"><span data-stu-id="233fb-112">Removes a job credential</span></span>

## <span data-ttu-id="233fb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="233fb-113">PARAMETERS</span></span>

### <span data-ttu-id="233fb-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="233fb-114">-AgentName</span></span>
<span data-ttu-id="233fb-115">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="233fb-115">The agent name</span></span>

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

### <span data-ttu-id="233fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="233fb-116">-DefaultProfile</span></span>
<span data-ttu-id="233fb-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="233fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="233fb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="233fb-118">-InputObject</span></span>
<span data-ttu-id="233fb-119">Oggetto credenziali processo</span><span class="sxs-lookup"><span data-stu-id="233fb-119">The job credential object</span></span>

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

### <span data-ttu-id="233fb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="233fb-120">-Name</span></span>
<span data-ttu-id="233fb-121">Nome della credenziale processo</span><span class="sxs-lookup"><span data-stu-id="233fb-121">The job credential name</span></span>

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

### <span data-ttu-id="233fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="233fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="233fb-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="233fb-123">The resource group name</span></span>

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

### <span data-ttu-id="233fb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="233fb-124">-ResourceId</span></span>
<span data-ttu-id="233fb-125">ID risorsa delle credenziali processo</span><span class="sxs-lookup"><span data-stu-id="233fb-125">The job credential resource id</span></span>

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

### <span data-ttu-id="233fb-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="233fb-126">-ServerName</span></span>
<span data-ttu-id="233fb-127">Nome del server</span><span class="sxs-lookup"><span data-stu-id="233fb-127">The server name</span></span>

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

### <span data-ttu-id="233fb-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="233fb-128">-Confirm</span></span>
<span data-ttu-id="233fb-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="233fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="233fb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="233fb-130">-WhatIf</span></span>
<span data-ttu-id="233fb-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="233fb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="233fb-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="233fb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="233fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="233fb-133">CommonParameters</span></span>
<span data-ttu-id="233fb-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="233fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="233fb-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="233fb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="233fb-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="233fb-136">INPUTS</span></span>

### <span data-ttu-id="233fb-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="233fb-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="233fb-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="233fb-138">OUTPUTS</span></span>

### <span data-ttu-id="233fb-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="233fb-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="233fb-140">Note</span><span class="sxs-lookup"><span data-stu-id="233fb-140">NOTES</span></span>

## <span data-ttu-id="233fb-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="233fb-141">RELATED LINKS</span></span>
