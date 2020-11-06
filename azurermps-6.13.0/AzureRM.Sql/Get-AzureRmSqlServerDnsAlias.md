---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: cc85bea2739c379e960ffee29250bdc172e36765
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514763"
---
# <span data-ttu-id="2b2d0-101">Get-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="2b2d0-101">Get-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="2b2d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b2d0-102">SYNOPSIS</span></span>
<span data-ttu-id="2b2d0-103">Ottiene o elenca gli alias di Azure SQL Server DNS.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b2d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b2d0-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b2d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b2d0-105">DESCRIPTION</span></span>
<span data-ttu-id="2b2d0-106">Ottenere l'alias DNS specifico di Azure SQL Server o elenca tutti gli alias DNS del server per il server</span><span class="sxs-lookup"><span data-stu-id="2b2d0-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="2b2d0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b2d0-107">EXAMPLES</span></span>

### <span data-ttu-id="2b2d0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2b2d0-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="2b2d0-109">Elenca tutti gli alias DNS del server per il server specifico</span><span class="sxs-lookup"><span data-stu-id="2b2d0-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="2b2d0-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2b2d0-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="2b2d0-111">Ottiene l'alias DNS del server specificato dal nome del server e dell'alias</span><span class="sxs-lookup"><span data-stu-id="2b2d0-111">Gets Server DNS Alias specified by server and alias name</span></span>

## <span data-ttu-id="2b2d0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b2d0-112">PARAMETERS</span></span>

### <span data-ttu-id="2b2d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b2d0-113">-DefaultProfile</span></span>
<span data-ttu-id="2b2d0-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b2d0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b2d0-115">-Name</span></span>
<span data-ttu-id="2b2d0-116">Nome dell'alias DNS di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-116">The Azure Sql Server DNS Alias name.</span></span>

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

### <span data-ttu-id="2b2d0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b2d0-117">-ResourceGroupName</span></span>
<span data-ttu-id="2b2d0-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="2b2d0-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2b2d0-119">-ServerName</span></span>
<span data-ttu-id="2b2d0-120">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="2b2d0-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b2d0-121">-Confirm</span></span>
<span data-ttu-id="2b2d0-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b2d0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b2d0-123">-WhatIf</span></span>
<span data-ttu-id="2b2d0-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b2d0-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b2d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b2d0-126">CommonParameters</span></span>
<span data-ttu-id="2b2d0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b2d0-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b2d0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b2d0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b2d0-129">INPUTS</span></span>

### <span data-ttu-id="2b2d0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2b2d0-130">System.String</span></span>

## <span data-ttu-id="2b2d0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b2d0-131">OUTPUTS</span></span>

### <span data-ttu-id="2b2d0-132">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="2b2d0-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="2b2d0-133">Note</span><span class="sxs-lookup"><span data-stu-id="2b2d0-133">NOTES</span></span>

## <span data-ttu-id="2b2d0-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b2d0-134">RELATED LINKS</span></span>
