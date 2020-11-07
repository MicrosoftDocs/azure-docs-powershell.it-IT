---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 60790af3396177e2885b4a83fda4d24db8c4e4d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676837"
---
# <span data-ttu-id="1250f-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="1250f-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="1250f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1250f-102">SYNOPSIS</span></span>
<span data-ttu-id="1250f-103">Questo comando crea un nuovo alias DNS di SQL Server di Azure.</span><span class="sxs-lookup"><span data-stu-id="1250f-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="1250f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1250f-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1250f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1250f-105">DESCRIPTION</span></span>
<span data-ttu-id="1250f-106">Crea un nuovo alias DNS di SQL Server di Azure che punta al server specificato.</span><span class="sxs-lookup"><span data-stu-id="1250f-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="1250f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1250f-107">EXAMPLES</span></span>

### <span data-ttu-id="1250f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1250f-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="1250f-109">Questo comando crea l'alias DNS di Azure SQL Server con il nome aliasname che punta al server nomeserver</span><span class="sxs-lookup"><span data-stu-id="1250f-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="1250f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1250f-110">PARAMETERS</span></span>

### <span data-ttu-id="1250f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1250f-111">-AsJob</span></span>
<span data-ttu-id="1250f-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1250f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1250f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1250f-113">-DefaultProfile</span></span>
<span data-ttu-id="1250f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1250f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1250f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1250f-115">-Name</span></span>
<span data-ttu-id="1250f-116">Nome dell'alias DNS di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1250f-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1250f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1250f-117">-ResourceGroupName</span></span>
<span data-ttu-id="1250f-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1250f-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1250f-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="1250f-119">-ServerName</span></span>
<span data-ttu-id="1250f-120">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1250f-120">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1250f-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1250f-121">-Confirm</span></span>
<span data-ttu-id="1250f-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1250f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1250f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1250f-123">-WhatIf</span></span>
<span data-ttu-id="1250f-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1250f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1250f-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1250f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1250f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1250f-126">CommonParameters</span></span>
<span data-ttu-id="1250f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1250f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1250f-128">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1250f-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1250f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1250f-129">INPUTS</span></span>

### <span data-ttu-id="1250f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1250f-130">System.String</span></span>

## <span data-ttu-id="1250f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1250f-131">OUTPUTS</span></span>

### <span data-ttu-id="1250f-132">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="1250f-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="1250f-133">Note</span><span class="sxs-lookup"><span data-stu-id="1250f-133">NOTES</span></span>

## <span data-ttu-id="1250f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1250f-134">RELATED LINKS</span></span>
