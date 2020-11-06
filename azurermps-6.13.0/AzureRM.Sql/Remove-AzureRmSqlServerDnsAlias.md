---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 5afd12ac027b19f888eb6a5110db2179dd6df24d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521302"
---
# <span data-ttu-id="06acf-101">Remove-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="06acf-101">Remove-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="06acf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06acf-102">SYNOPSIS</span></span>
<span data-ttu-id="06acf-103">Rimuove l'alias DNS di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="06acf-103">Removes Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06acf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06acf-104">SYNTAX</span></span>

### <span data-ttu-id="06acf-105">Rimuovere un alias DNS del server dai parametri di input dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="06acf-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzureRmSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06acf-106">Rimuovere un alias DNS del server dalla definizione dell'istanza di AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="06acf-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzureRmSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06acf-107">Rimuovere un alias DNS del server da un ID di risorsa Azure</span><span class="sxs-lookup"><span data-stu-id="06acf-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzureRmSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06acf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06acf-108">DESCRIPTION</span></span>
<span data-ttu-id="06acf-109">Questo comando rimuove l'alias DNS di Azure SQL Server dal server lasciando intatto il server.</span><span class="sxs-lookup"><span data-stu-id="06acf-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="06acf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06acf-110">EXAMPLES</span></span>

### <span data-ttu-id="06acf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="06acf-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="06acf-112">Rimuove l'alias DNS di Azure SQL Server con il nome aliasname dal server con il nome nomeserver</span><span class="sxs-lookup"><span data-stu-id="06acf-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="06acf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06acf-113">PARAMETERS</span></span>

### <span data-ttu-id="06acf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06acf-114">-AsJob</span></span>
<span data-ttu-id="06acf-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="06acf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06acf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06acf-116">-DefaultProfile</span></span>
<span data-ttu-id="06acf-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06acf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06acf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="06acf-118">-Force</span></span>
<span data-ttu-id="06acf-119">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="06acf-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="06acf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06acf-120">-InputObject</span></span>
<span data-ttu-id="06acf-121">Oggetto alias DNS del server da rimuovere</span><span class="sxs-lookup"><span data-stu-id="06acf-121">The Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="06acf-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="06acf-122">-Name</span></span>
<span data-ttu-id="06acf-123">Nome dell'alias DNS di Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="06acf-123">Azure Sql Server Dns Alias name</span></span>

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

### <span data-ttu-id="06acf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06acf-124">-ResourceGroupName</span></span>
<span data-ttu-id="06acf-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="06acf-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="06acf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06acf-126">-ResourceId</span></span>
<span data-ttu-id="06acf-127">ID risorsa dell'oggetto alias DNS del server da rimuovere</span><span class="sxs-lookup"><span data-stu-id="06acf-127">The resource id of Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="06acf-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="06acf-128">-ServerName</span></span>
<span data-ttu-id="06acf-129">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="06acf-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="06acf-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06acf-130">-Confirm</span></span>
<span data-ttu-id="06acf-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06acf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06acf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06acf-132">-WhatIf</span></span>
<span data-ttu-id="06acf-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06acf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06acf-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06acf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06acf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06acf-135">CommonParameters</span></span>
<span data-ttu-id="06acf-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06acf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06acf-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06acf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06acf-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06acf-138">INPUTS</span></span>

### <span data-ttu-id="06acf-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="06acf-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>
<span data-ttu-id="06acf-140">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="06acf-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="06acf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="06acf-141">System.String</span></span>

## <span data-ttu-id="06acf-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06acf-142">OUTPUTS</span></span>

### <span data-ttu-id="06acf-143">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="06acf-143">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="06acf-144">Note</span><span class="sxs-lookup"><span data-stu-id="06acf-144">NOTES</span></span>

## <span data-ttu-id="06acf-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06acf-145">RELATED LINKS</span></span>
