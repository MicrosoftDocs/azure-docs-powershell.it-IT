---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: d611f0bc14d657f47881cbdfbb1326111873114a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197678"
---
# <span data-ttu-id="9661f-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="9661f-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="9661f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9661f-102">SYNOPSIS</span></span>
<span data-ttu-id="9661f-103">Rimuove l'alias DNS SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="9661f-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="9661f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9661f-104">SYNTAX</span></span>

### <span data-ttu-id="9661f-105">Rimuovere un alias dns del server dai parametri di input del cmdlet</span><span class="sxs-lookup"><span data-stu-id="9661f-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9661f-106">Rimuovere un alias dns del server dalla definizione di istanza di AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="9661f-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9661f-107">Rimuovere un alias dns del server da un ID di risorsa di Azure</span><span class="sxs-lookup"><span data-stu-id="9661f-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9661f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9661f-108">DESCRIPTION</span></span>
<span data-ttu-id="9661f-109">Questo comando rimuove Azure SQL Server alias DNS dal server lasciando intatto il server.</span><span class="sxs-lookup"><span data-stu-id="9661f-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="9661f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9661f-110">EXAMPLES</span></span>

### <span data-ttu-id="9661f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9661f-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="9661f-112">Rimuove l'SQL Server DNS di Azure con il nome aliasName dal server con il nome serverName</span><span class="sxs-lookup"><span data-stu-id="9661f-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="9661f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9661f-113">PARAMETERS</span></span>

### <span data-ttu-id="9661f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9661f-114">-AsJob</span></span>
<span data-ttu-id="9661f-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9661f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9661f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9661f-116">-DefaultProfile</span></span>
<span data-ttu-id="9661f-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9661f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9661f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9661f-118">-Force</span></span>
<span data-ttu-id="9661f-119">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="9661f-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9661f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9661f-120">-InputObject</span></span>
<span data-ttu-id="9661f-121">Oggetto Alias Dns server da rimuovere</span><span class="sxs-lookup"><span data-stu-id="9661f-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9661f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9661f-122">-Name</span></span>
<span data-ttu-id="9661f-123">Nome alias Dns del server DNS di Azure</span><span class="sxs-lookup"><span data-stu-id="9661f-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9661f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9661f-124">-ResourceGroupName</span></span>
<span data-ttu-id="9661f-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9661f-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9661f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9661f-126">-ResourceId</span></span>
<span data-ttu-id="9661f-127">ID risorsa dell'oggetto Alias DNS server da rimuovere</span><span class="sxs-lookup"><span data-stu-id="9661f-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9661f-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9661f-128">-ServerName</span></span>
<span data-ttu-id="9661f-129">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9661f-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9661f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9661f-130">-Confirm</span></span>
<span data-ttu-id="9661f-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9661f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9661f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9661f-132">-WhatIf</span></span>
<span data-ttu-id="9661f-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9661f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9661f-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9661f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9661f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9661f-135">CommonParameters</span></span>
<span data-ttu-id="9661f-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9661f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9661f-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9661f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9661f-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="9661f-138">INPUTS</span></span>

### <span data-ttu-id="9661f-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="9661f-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="9661f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9661f-140">System.String</span></span>

## <span data-ttu-id="9661f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9661f-141">OUTPUTS</span></span>

### <span data-ttu-id="9661f-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="9661f-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="9661f-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="9661f-143">NOTES</span></span>

## <span data-ttu-id="9661f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9661f-144">RELATED LINKS</span></span>
