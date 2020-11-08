---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189274"
---
# <span data-ttu-id="94f0d-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="94f0d-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="94f0d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="94f0d-103">Rimuove le credenziali per i processi elastici</span><span class="sxs-lookup"><span data-stu-id="94f0d-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="94f0d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94f0d-104">SYNTAX</span></span>

### <span data-ttu-id="94f0d-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94f0d-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f0d-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="94f0d-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f0d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="94f0d-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f0d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94f0d-108">DESCRIPTION</span></span>
<span data-ttu-id="94f0d-109">Il cmdlet Remove-AzSqlElasticJobCredential rimuove le credenziali di un processo</span><span class="sxs-lookup"><span data-stu-id="94f0d-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="94f0d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94f0d-110">EXAMPLES</span></span>

### <span data-ttu-id="94f0d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94f0d-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="94f0d-112">Rimuove le credenziali di un processo</span><span class="sxs-lookup"><span data-stu-id="94f0d-112">Removes a job credential</span></span>

## <span data-ttu-id="94f0d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94f0d-113">PARAMETERS</span></span>

### <span data-ttu-id="94f0d-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="94f0d-114">-AgentName</span></span>
<span data-ttu-id="94f0d-115">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="94f0d-115">The agent name</span></span>

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

### <span data-ttu-id="94f0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f0d-116">-DefaultProfile</span></span>
<span data-ttu-id="94f0d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94f0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94f0d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94f0d-118">-InputObject</span></span>
<span data-ttu-id="94f0d-119">Oggetto credenziali processo</span><span class="sxs-lookup"><span data-stu-id="94f0d-119">The job credential object</span></span>

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

### <span data-ttu-id="94f0d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="94f0d-120">-Name</span></span>
<span data-ttu-id="94f0d-121">Nome della credenziale processo</span><span class="sxs-lookup"><span data-stu-id="94f0d-121">The job credential name</span></span>

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

### <span data-ttu-id="94f0d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f0d-122">-ResourceGroupName</span></span>
<span data-ttu-id="94f0d-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="94f0d-123">The resource group name</span></span>

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

### <span data-ttu-id="94f0d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94f0d-124">-ResourceId</span></span>
<span data-ttu-id="94f0d-125">ID risorsa delle credenziali processo</span><span class="sxs-lookup"><span data-stu-id="94f0d-125">The job credential resource id</span></span>

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

### <span data-ttu-id="94f0d-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="94f0d-126">-ServerName</span></span>
<span data-ttu-id="94f0d-127">Nome del server</span><span class="sxs-lookup"><span data-stu-id="94f0d-127">The server name</span></span>

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

### <span data-ttu-id="94f0d-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="94f0d-128">-Confirm</span></span>
<span data-ttu-id="94f0d-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94f0d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f0d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f0d-130">-WhatIf</span></span>
<span data-ttu-id="94f0d-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94f0d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f0d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94f0d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f0d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f0d-133">CommonParameters</span></span>
<span data-ttu-id="94f0d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f0d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f0d-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94f0d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f0d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94f0d-136">INPUTS</span></span>

### <span data-ttu-id="94f0d-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="94f0d-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="94f0d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94f0d-138">OUTPUTS</span></span>

### <span data-ttu-id="94f0d-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="94f0d-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="94f0d-140">Note</span><span class="sxs-lookup"><span data-stu-id="94f0d-140">NOTES</span></span>

## <span data-ttu-id="94f0d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94f0d-141">RELATED LINKS</span></span>
