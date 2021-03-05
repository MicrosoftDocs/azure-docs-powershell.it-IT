---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: 07065c18b9e06f75863ddd41f8a6f0155a3699f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967389"
---
# <span data-ttu-id="50958-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="50958-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="50958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50958-102">SYNOPSIS</span></span>
<span data-ttu-id="50958-103">Rimuove l'alias DNS SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="50958-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="50958-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50958-104">SYNTAX</span></span>

### <span data-ttu-id="50958-105">Rimuovere un alias dns del server dai parametri di input del cmdlet</span><span class="sxs-lookup"><span data-stu-id="50958-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50958-106">Rimuovere un alias dns del server dalla definizione di istanza di AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="50958-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50958-107">Rimuovere un alias dns del server da un ID di risorsa di Azure</span><span class="sxs-lookup"><span data-stu-id="50958-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50958-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="50958-108">DESCRIPTION</span></span>
<span data-ttu-id="50958-109">Questo comando rimuove Azure SQL Server alias DNS dal server lasciando intatto il server.</span><span class="sxs-lookup"><span data-stu-id="50958-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="50958-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50958-110">EXAMPLES</span></span>

### <span data-ttu-id="50958-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50958-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="50958-112">Rimuove l'SQL Server DNS di Azure con il nome aliasName dal server con il nome serverName</span><span class="sxs-lookup"><span data-stu-id="50958-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="50958-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50958-113">PARAMETERS</span></span>

### <span data-ttu-id="50958-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50958-114">-AsJob</span></span>
<span data-ttu-id="50958-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="50958-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50958-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50958-116">-DefaultProfile</span></span>
<span data-ttu-id="50958-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50958-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50958-118">-Force</span><span class="sxs-lookup"><span data-stu-id="50958-118">-Force</span></span>
<span data-ttu-id="50958-119">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="50958-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="50958-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50958-120">-InputObject</span></span>
<span data-ttu-id="50958-121">Oggetto Alias Dns server da rimuovere</span><span class="sxs-lookup"><span data-stu-id="50958-121">The Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="50958-122">-Name</span><span class="sxs-lookup"><span data-stu-id="50958-122">-Name</span></span>
<span data-ttu-id="50958-123">Nome alias Dns del server DNS di Azure</span><span class="sxs-lookup"><span data-stu-id="50958-123">Azure Sql Server Dns Alias name</span></span>

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

### <span data-ttu-id="50958-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50958-124">-ResourceGroupName</span></span>
<span data-ttu-id="50958-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50958-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="50958-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50958-126">-ResourceId</span></span>
<span data-ttu-id="50958-127">ID risorsa dell'oggetto Alias DNS server da rimuovere</span><span class="sxs-lookup"><span data-stu-id="50958-127">The resource id of Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="50958-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="50958-128">-ServerName</span></span>
<span data-ttu-id="50958-129">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="50958-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="50958-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50958-130">-Confirm</span></span>
<span data-ttu-id="50958-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50958-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50958-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50958-132">-WhatIf</span></span>
<span data-ttu-id="50958-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50958-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50958-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50958-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50958-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50958-135">CommonParameters</span></span>
<span data-ttu-id="50958-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50958-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50958-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="50958-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50958-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="50958-138">INPUTS</span></span>

### <span data-ttu-id="50958-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="50958-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="50958-140">System.String</span><span class="sxs-lookup"><span data-stu-id="50958-140">System.String</span></span>

## <span data-ttu-id="50958-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50958-141">OUTPUTS</span></span>

### <span data-ttu-id="50958-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="50958-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="50958-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="50958-143">NOTES</span></span>

## <span data-ttu-id="50958-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50958-144">RELATED LINKS</span></span>
