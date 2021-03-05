---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: bbc941c260579fb7fdb437f0b30002999635b8eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970174"
---
# <span data-ttu-id="400b6-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="400b6-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="400b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="400b6-102">SYNOPSIS</span></span>
<span data-ttu-id="400b6-103">Modifica il server a cui l'alias DNS SQL Server Azure fa riferimento</span><span class="sxs-lookup"><span data-stu-id="400b6-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="400b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="400b6-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="400b6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="400b6-105">DESCRIPTION</span></span>
<span data-ttu-id="400b6-106">Questo comando sta aggiornando il server a cui punta l'alias.</span><span class="sxs-lookup"><span data-stu-id="400b6-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="400b6-107">Questo comando deve essere inviato durante l'accesso all'abbonamento in cui si trova il nuovo server a cui punta l'alias.</span><span class="sxs-lookup"><span data-stu-id="400b6-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="400b6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="400b6-108">EXAMPLES</span></span>

### <span data-ttu-id="400b6-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="400b6-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="400b6-110">Questo comando sta aggiornando l'alias che in precedenza puntava a oldServer in modo che punti al server newServer</span><span class="sxs-lookup"><span data-stu-id="400b6-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="400b6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="400b6-111">PARAMETERS</span></span>

### <span data-ttu-id="400b6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="400b6-112">-AsJob</span></span>
<span data-ttu-id="400b6-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="400b6-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="400b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="400b6-114">-DefaultProfile</span></span>
<span data-ttu-id="400b6-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="400b6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="400b6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="400b6-116">-Name</span></span>
<span data-ttu-id="400b6-117">Nome alias DNS del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="400b6-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="400b6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="400b6-118">-ResourceGroupName</span></span>
<span data-ttu-id="400b6-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="400b6-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="400b6-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="400b6-120">-SourceServerName</span></span>
<span data-ttu-id="400b6-121">Nome del server SQL di Azure a cui punta attualmente l'alias.</span><span class="sxs-lookup"><span data-stu-id="400b6-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="400b6-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="400b6-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="400b6-123">Nome del gruppo di risorse del server di origine.</span><span class="sxs-lookup"><span data-stu-id="400b6-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="400b6-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="400b6-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="400b6-125">ID sottoscrizione del server di origine</span><span class="sxs-lookup"><span data-stu-id="400b6-125">The subscription id of the source server</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400b6-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="400b6-126">-TargetServerName</span></span>
<span data-ttu-id="400b6-127">Nome del server SQL di Azure a cui deve puntare l'alias.</span><span class="sxs-lookup"><span data-stu-id="400b6-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="400b6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="400b6-128">-Confirm</span></span>
<span data-ttu-id="400b6-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="400b6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="400b6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="400b6-130">-WhatIf</span></span>
<span data-ttu-id="400b6-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="400b6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="400b6-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="400b6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="400b6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="400b6-133">CommonParameters</span></span>
<span data-ttu-id="400b6-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="400b6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="400b6-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="400b6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="400b6-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="400b6-136">INPUTS</span></span>

### <span data-ttu-id="400b6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="400b6-137">System.String</span></span>

## <span data-ttu-id="400b6-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="400b6-138">OUTPUTS</span></span>

### <span data-ttu-id="400b6-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="400b6-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="400b6-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="400b6-140">NOTES</span></span>

## <span data-ttu-id="400b6-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="400b6-141">RELATED LINKS</span></span>
