---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 49a175606526979acb4c44ddc4cb23ca7bbc33ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978078"
---
# <span data-ttu-id="9eda3-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="9eda3-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="9eda3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eda3-102">SYNOPSIS</span></span>
<span data-ttu-id="9eda3-103">Ottiene o elenca l'alias DNS SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="9eda3-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="9eda3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9eda3-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eda3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9eda3-105">DESCRIPTION</span></span>
<span data-ttu-id="9eda3-106">Ottenere lo specifico alias DNS SQL Server Azure o elencare tutti gli alias DNS del server per il server</span><span class="sxs-lookup"><span data-stu-id="9eda3-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="9eda3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9eda3-107">EXAMPLES</span></span>

### <span data-ttu-id="9eda3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9eda3-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="9eda3-109">Elenca tutti gli alias DNS del server per il server specifico</span><span class="sxs-lookup"><span data-stu-id="9eda3-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="9eda3-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9eda3-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="9eda3-111">Ottiene l'alias DNS del server specificato dal nome del server e dell'alias</span><span class="sxs-lookup"><span data-stu-id="9eda3-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="9eda3-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9eda3-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="9eda3-113">Elenca tutti gli alias DNS del server per il server specifico che iniziano con "dnsaliasname".</span><span class="sxs-lookup"><span data-stu-id="9eda3-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="9eda3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9eda3-114">PARAMETERS</span></span>

### <span data-ttu-id="9eda3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eda3-115">-DefaultProfile</span></span>
<span data-ttu-id="9eda3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9eda3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eda3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9eda3-117">-Name</span></span>
<span data-ttu-id="9eda3-118">Nome alias DNS del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9eda3-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eda3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eda3-119">-ResourceGroupName</span></span>
<span data-ttu-id="9eda3-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9eda3-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="9eda3-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9eda3-121">-ServerName</span></span>
<span data-ttu-id="9eda3-122">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9eda3-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="9eda3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9eda3-123">-Confirm</span></span>
<span data-ttu-id="9eda3-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9eda3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eda3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eda3-125">-WhatIf</span></span>
<span data-ttu-id="9eda3-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9eda3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eda3-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9eda3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eda3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eda3-128">CommonParameters</span></span>
<span data-ttu-id="9eda3-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eda3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eda3-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9eda3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eda3-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="9eda3-131">INPUTS</span></span>

### <span data-ttu-id="9eda3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9eda3-132">System.String</span></span>

## <span data-ttu-id="9eda3-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9eda3-133">OUTPUTS</span></span>

### <span data-ttu-id="9eda3-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="9eda3-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="9eda3-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="9eda3-135">NOTES</span></span>

## <span data-ttu-id="9eda3-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9eda3-136">RELATED LINKS</span></span>
