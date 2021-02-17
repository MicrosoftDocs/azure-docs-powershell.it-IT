---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188086"
---
# <span data-ttu-id="c9785-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="c9785-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="c9785-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9785-102">SYNOPSIS</span></span>
<span data-ttu-id="c9785-103">Ottiene o elenca l'alias DNS SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="c9785-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="c9785-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9785-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9785-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c9785-105">DESCRIPTION</span></span>
<span data-ttu-id="c9785-106">Ottenere lo specifico alias DNS SQL Server Azure o elencare tutti gli alias DNS del server per il server</span><span class="sxs-lookup"><span data-stu-id="c9785-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="c9785-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9785-107">EXAMPLES</span></span>

### <span data-ttu-id="c9785-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c9785-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="c9785-109">Elenca tutti gli alias DNS del server per il server specifico</span><span class="sxs-lookup"><span data-stu-id="c9785-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="c9785-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c9785-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="c9785-111">Ottiene l'alias DNS del server specificato dal nome del server e dell'alias</span><span class="sxs-lookup"><span data-stu-id="c9785-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="c9785-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c9785-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="c9785-113">Elenca tutti gli alias DNS del server per il server specifico che iniziano con "dnsaliasname".</span><span class="sxs-lookup"><span data-stu-id="c9785-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="c9785-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9785-114">PARAMETERS</span></span>

### <span data-ttu-id="c9785-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9785-115">-DefaultProfile</span></span>
<span data-ttu-id="c9785-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9785-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9785-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c9785-117">-Name</span></span>
<span data-ttu-id="c9785-118">Nome alias DNS del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9785-118">The Azure Sql Server DNS Alias name.</span></span>

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

### <span data-ttu-id="c9785-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9785-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9785-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c9785-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="c9785-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c9785-121">-ServerName</span></span>
<span data-ttu-id="c9785-122">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9785-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c9785-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9785-123">-Confirm</span></span>
<span data-ttu-id="c9785-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9785-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9785-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9785-125">-WhatIf</span></span>
<span data-ttu-id="c9785-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9785-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9785-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9785-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9785-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9785-128">CommonParameters</span></span>
<span data-ttu-id="c9785-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9785-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9785-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c9785-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9785-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="c9785-131">INPUTS</span></span>

### <span data-ttu-id="c9785-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c9785-132">System.String</span></span>

## <span data-ttu-id="c9785-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9785-133">OUTPUTS</span></span>

### <span data-ttu-id="c9785-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="c9785-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="c9785-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="c9785-135">NOTES</span></span>

## <span data-ttu-id="c9785-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9785-136">RELATED LINKS</span></span>
