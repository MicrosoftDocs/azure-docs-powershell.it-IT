---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 6c18639e3c717ced8ed107ce3604e20639d87682
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513363"
---
# <span data-ttu-id="25a88-101">Set-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="25a88-101">Set-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="25a88-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="25a88-102">SYNOPSIS</span></span>
<span data-ttu-id="25a88-103">Modifica il server in cui punta l'alias di Azure SQL Server DNS</span><span class="sxs-lookup"><span data-stu-id="25a88-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25a88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25a88-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25a88-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25a88-105">DESCRIPTION</span></span>
<span data-ttu-id="25a88-106">Questo comando Aggiorna il server in cui punta l'alias.</span><span class="sxs-lookup"><span data-stu-id="25a88-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="25a88-107">Questo comando deve essere emesso durante l'accesso all'abbonamento in cui si trova il nuovo server a cui punta l'alias.</span><span class="sxs-lookup"><span data-stu-id="25a88-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="25a88-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25a88-108">EXAMPLES</span></span>

### <span data-ttu-id="25a88-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="25a88-109">Example 1</span></span>
```
PS C:\> Set-AzureRmSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="25a88-110">Questo comando Aggiorna l'alias che in precedenza puntava a oldServer in modo che punti al server newServer</span><span class="sxs-lookup"><span data-stu-id="25a88-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="25a88-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="25a88-111">PARAMETERS</span></span>

### <span data-ttu-id="25a88-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25a88-112">-AsJob</span></span>
<span data-ttu-id="25a88-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="25a88-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25a88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a88-114">-DefaultProfile</span></span>
<span data-ttu-id="25a88-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25a88-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25a88-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="25a88-116">-Name</span></span>
<span data-ttu-id="25a88-117">Nome dell'alias DNS di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="25a88-117">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="25a88-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25a88-118">-ResourceGroupName</span></span>
<span data-ttu-id="25a88-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25a88-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="25a88-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="25a88-120">-SourceServerName</span></span>
<span data-ttu-id="25a88-121">Nome di Azure SQL Server a cui è attualmente puntato l'alias.</span><span class="sxs-lookup"><span data-stu-id="25a88-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="25a88-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25a88-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="25a88-123">Il nome del gruppo di risorse del server di origine.</span><span class="sxs-lookup"><span data-stu-id="25a88-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="25a88-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25a88-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="25a88-125">ID sottoscrizione del server di origine</span><span class="sxs-lookup"><span data-stu-id="25a88-125">The subscription id of the source server</span></span>

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

### <span data-ttu-id="25a88-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="25a88-126">-TargetServerName</span></span>
<span data-ttu-id="25a88-127">Il nome di Azure SQL Server a cui deve puntare l'alias.</span><span class="sxs-lookup"><span data-stu-id="25a88-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="25a88-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="25a88-128">-Confirm</span></span>
<span data-ttu-id="25a88-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25a88-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25a88-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25a88-130">-WhatIf</span></span>
<span data-ttu-id="25a88-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25a88-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25a88-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25a88-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25a88-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a88-133">CommonParameters</span></span>
<span data-ttu-id="25a88-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25a88-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a88-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25a88-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a88-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="25a88-136">INPUTS</span></span>

### <span data-ttu-id="25a88-137">System. String</span><span class="sxs-lookup"><span data-stu-id="25a88-137">System.String</span></span>

## <span data-ttu-id="25a88-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25a88-138">OUTPUTS</span></span>

### <span data-ttu-id="25a88-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="25a88-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="25a88-140">Note</span><span class="sxs-lookup"><span data-stu-id="25a88-140">NOTES</span></span>

## <span data-ttu-id="25a88-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25a88-141">RELATED LINKS</span></span>
