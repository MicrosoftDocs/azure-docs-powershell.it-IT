---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 7022f8655e1b87bc55ddd90cbd0aca512eeec0a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676711"
---
# <span data-ttu-id="02d63-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="02d63-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="02d63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02d63-102">SYNOPSIS</span></span>
<span data-ttu-id="02d63-103">Modifica il server in cui punta l'alias di Azure SQL Server DNS</span><span class="sxs-lookup"><span data-stu-id="02d63-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="02d63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02d63-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02d63-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02d63-105">DESCRIPTION</span></span>
<span data-ttu-id="02d63-106">Questo comando Aggiorna il server in cui punta l'alias.</span><span class="sxs-lookup"><span data-stu-id="02d63-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="02d63-107">Questo comando deve essere emesso durante l'accesso all'abbonamento in cui si trova il nuovo server a cui punta l'alias.</span><span class="sxs-lookup"><span data-stu-id="02d63-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="02d63-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02d63-108">EXAMPLES</span></span>

### <span data-ttu-id="02d63-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="02d63-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="02d63-110">Questo comando Aggiorna l'alias che in precedenza puntava a oldServer in modo che punti al server newServer</span><span class="sxs-lookup"><span data-stu-id="02d63-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="02d63-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02d63-111">PARAMETERS</span></span>

### <span data-ttu-id="02d63-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02d63-112">-AsJob</span></span>
<span data-ttu-id="02d63-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="02d63-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02d63-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d63-114">-DefaultProfile</span></span>
<span data-ttu-id="02d63-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="02d63-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02d63-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="02d63-116">-Name</span></span>
<span data-ttu-id="02d63-117">Nome dell'alias DNS di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="02d63-117">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="02d63-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d63-118">-ResourceGroupName</span></span>
<span data-ttu-id="02d63-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="02d63-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="02d63-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="02d63-120">-SourceServerName</span></span>
<span data-ttu-id="02d63-121">Nome di Azure SQL Server a cui è attualmente puntato l'alias.</span><span class="sxs-lookup"><span data-stu-id="02d63-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="02d63-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d63-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="02d63-123">Il nome del gruppo di risorse del server di origine.</span><span class="sxs-lookup"><span data-stu-id="02d63-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="02d63-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02d63-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="02d63-125">ID sottoscrizione del server di origine</span><span class="sxs-lookup"><span data-stu-id="02d63-125">The subscription id of the source server</span></span>

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

### <span data-ttu-id="02d63-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="02d63-126">-TargetServerName</span></span>
<span data-ttu-id="02d63-127">Il nome di Azure SQL Server a cui deve puntare l'alias.</span><span class="sxs-lookup"><span data-stu-id="02d63-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="02d63-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="02d63-128">-Confirm</span></span>
<span data-ttu-id="02d63-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02d63-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02d63-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02d63-130">-WhatIf</span></span>
<span data-ttu-id="02d63-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02d63-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02d63-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02d63-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02d63-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d63-133">CommonParameters</span></span>
<span data-ttu-id="02d63-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d63-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d63-135">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02d63-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d63-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02d63-136">INPUTS</span></span>

### <span data-ttu-id="02d63-137">System. String</span><span class="sxs-lookup"><span data-stu-id="02d63-137">System.String</span></span>

## <span data-ttu-id="02d63-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02d63-138">OUTPUTS</span></span>

### <span data-ttu-id="02d63-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="02d63-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="02d63-140">Note</span><span class="sxs-lookup"><span data-stu-id="02d63-140">NOTES</span></span>

## <span data-ttu-id="02d63-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02d63-141">RELATED LINKS</span></span>