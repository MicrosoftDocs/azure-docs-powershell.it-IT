---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 791658e9f4f10fdbb8b1000d6b1bc88d392aaf46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187958"
---
# <span data-ttu-id="6183d-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="6183d-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="6183d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6183d-102">SYNOPSIS</span></span>
<span data-ttu-id="6183d-103">Modifica il server a cui l'alias DNS SQL Server Azure fa riferimento</span><span class="sxs-lookup"><span data-stu-id="6183d-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="6183d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6183d-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6183d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6183d-105">DESCRIPTION</span></span>
<span data-ttu-id="6183d-106">Questo comando sta aggiornando il server a cui punta l'alias.</span><span class="sxs-lookup"><span data-stu-id="6183d-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="6183d-107">Questo comando deve essere inviato durante l'accesso all'abbonamento in cui si trova il nuovo server a cui punta l'alias.</span><span class="sxs-lookup"><span data-stu-id="6183d-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="6183d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6183d-108">EXAMPLES</span></span>

### <span data-ttu-id="6183d-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6183d-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="6183d-110">Questo comando sta aggiornando l'alias che in precedenza puntava a oldServer in modo che punti al server newServer</span><span class="sxs-lookup"><span data-stu-id="6183d-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="6183d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6183d-111">PARAMETERS</span></span>

### <span data-ttu-id="6183d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6183d-112">-AsJob</span></span>
<span data-ttu-id="6183d-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6183d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6183d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6183d-114">-DefaultProfile</span></span>
<span data-ttu-id="6183d-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6183d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6183d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6183d-116">-Name</span></span>
<span data-ttu-id="6183d-117">Nome alias DNS del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="6183d-117">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="6183d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6183d-118">-ResourceGroupName</span></span>
<span data-ttu-id="6183d-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6183d-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="6183d-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="6183d-120">-SourceServerName</span></span>
<span data-ttu-id="6183d-121">Nome del server SQL di Azure a cui punta attualmente l'alias.</span><span class="sxs-lookup"><span data-stu-id="6183d-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="6183d-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6183d-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="6183d-123">Nome del gruppo di risorse del server di origine.</span><span class="sxs-lookup"><span data-stu-id="6183d-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="6183d-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6183d-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="6183d-125">ID sottoscrizione del server di origine</span><span class="sxs-lookup"><span data-stu-id="6183d-125">The subscription id of the source server</span></span>

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

### <span data-ttu-id="6183d-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="6183d-126">-TargetServerName</span></span>
<span data-ttu-id="6183d-127">Nome del server SQL di Azure a cui deve puntare l'alias.</span><span class="sxs-lookup"><span data-stu-id="6183d-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="6183d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6183d-128">-Confirm</span></span>
<span data-ttu-id="6183d-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6183d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6183d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6183d-130">-WhatIf</span></span>
<span data-ttu-id="6183d-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6183d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6183d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6183d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6183d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6183d-133">CommonParameters</span></span>
<span data-ttu-id="6183d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6183d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6183d-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6183d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6183d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="6183d-136">INPUTS</span></span>

### <span data-ttu-id="6183d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6183d-137">System.String</span></span>

## <span data-ttu-id="6183d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6183d-138">OUTPUTS</span></span>

### <span data-ttu-id="6183d-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="6183d-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="6183d-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="6183d-140">NOTES</span></span>

## <span data-ttu-id="6183d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6183d-141">RELATED LINKS</span></span>
