---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350056"
---
# <span data-ttu-id="41551-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="41551-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="41551-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41551-102">SYNOPSIS</span></span>
<span data-ttu-id="41551-103">Ottiene o elenca gli alias di Azure SQL Server DNS.</span><span class="sxs-lookup"><span data-stu-id="41551-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="41551-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41551-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41551-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41551-105">DESCRIPTION</span></span>
<span data-ttu-id="41551-106">Ottenere l'alias DNS specifico di Azure SQL Server o elenca tutti gli alias DNS del server per il server</span><span class="sxs-lookup"><span data-stu-id="41551-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="41551-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41551-107">EXAMPLES</span></span>

### <span data-ttu-id="41551-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="41551-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="41551-109">Elenca tutti gli alias DNS del server per il server specifico</span><span class="sxs-lookup"><span data-stu-id="41551-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="41551-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="41551-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="41551-111">Ottiene l'alias DNS del server specificato dal nome del server e dell'alias</span><span class="sxs-lookup"><span data-stu-id="41551-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="41551-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="41551-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="41551-113">Elenca tutti gli alias DNS del server per il server specifico che iniziano con "dnsaliasname".</span><span class="sxs-lookup"><span data-stu-id="41551-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="41551-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41551-114">PARAMETERS</span></span>

### <span data-ttu-id="41551-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41551-115">-DefaultProfile</span></span>
<span data-ttu-id="41551-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41551-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41551-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="41551-117">-Name</span></span>
<span data-ttu-id="41551-118">Nome dell'alias DNS di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="41551-118">The Azure Sql Server DNS Alias name.</span></span>

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

### <span data-ttu-id="41551-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41551-119">-ResourceGroupName</span></span>
<span data-ttu-id="41551-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41551-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="41551-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="41551-121">-ServerName</span></span>
<span data-ttu-id="41551-122">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="41551-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="41551-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="41551-123">-Confirm</span></span>
<span data-ttu-id="41551-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41551-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41551-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41551-125">-WhatIf</span></span>
<span data-ttu-id="41551-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41551-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41551-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41551-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41551-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41551-128">CommonParameters</span></span>
<span data-ttu-id="41551-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41551-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41551-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41551-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41551-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41551-131">INPUTS</span></span>

### <span data-ttu-id="41551-132">System. String</span><span class="sxs-lookup"><span data-stu-id="41551-132">System.String</span></span>

## <span data-ttu-id="41551-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41551-133">OUTPUTS</span></span>

### <span data-ttu-id="41551-134">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="41551-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="41551-135">Note</span><span class="sxs-lookup"><span data-stu-id="41551-135">NOTES</span></span>

## <span data-ttu-id="41551-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41551-136">RELATED LINKS</span></span>
