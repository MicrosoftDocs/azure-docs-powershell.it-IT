---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: d57e73c71e95fe673f9b54d9129714ca22670d31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521950"
---
# <span data-ttu-id="17fa1-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="17fa1-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="17fa1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="17fa1-103">Rimuove un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="17fa1-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17fa1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17fa1-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17fa1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17fa1-105">DESCRIPTION</span></span>
<span data-ttu-id="17fa1-106">Il cmdlet **Remove-AzureRmSqlSyncMember** rimuove un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="17fa1-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="17fa1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17fa1-107">EXAMPLES</span></span>

### <span data-ttu-id="17fa1-108">Esempio 1: rimuovere un membro di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="17fa1-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="17fa1-109">Questo comando rimuove il membro di sincronizzazione di database SQL di Azure denominato syncMember01.</span><span class="sxs-lookup"><span data-stu-id="17fa1-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="17fa1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17fa1-110">PARAMETERS</span></span>

### <span data-ttu-id="17fa1-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="17fa1-111">-Confirm</span></span>
<span data-ttu-id="17fa1-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17fa1-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17fa1-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="17fa1-113">-DatabaseName</span></span>
<span data-ttu-id="17fa1-114">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="17fa1-114">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17fa1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="17fa1-115">-Force</span></span>
<span data-ttu-id="17fa1-116">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="17fa1-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="17fa1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="17fa1-117">-Name</span></span>
<span data-ttu-id="17fa1-118">Il nome del membro della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="17fa1-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17fa1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17fa1-119">-PassThru</span></span>
<span data-ttu-id="17fa1-120">Definisce se restituire il membro di sincronizzazione rimosso</span><span class="sxs-lookup"><span data-stu-id="17fa1-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="17fa1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17fa1-121">-ResourceGroupName</span></span>
<span data-ttu-id="17fa1-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="17fa1-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="17fa1-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="17fa1-123">-ServerName</span></span>
<span data-ttu-id="17fa1-124">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="17fa1-124">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17fa1-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="17fa1-125">-SyncGroupName</span></span>
<span data-ttu-id="17fa1-126">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="17fa1-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17fa1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17fa1-127">-WhatIf</span></span>
<span data-ttu-id="17fa1-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17fa1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17fa1-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17fa1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17fa1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17fa1-130">-DefaultProfile</span></span>
<span data-ttu-id="17fa1-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17fa1-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17fa1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fa1-132">CommonParameters</span></span>
<span data-ttu-id="17fa1-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17fa1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fa1-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17fa1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fa1-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17fa1-135">INPUTS</span></span>

## <span data-ttu-id="17fa1-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17fa1-136">OUTPUTS</span></span>

### <span data-ttu-id="17fa1-137">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="17fa1-137">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="17fa1-138">Note</span><span class="sxs-lookup"><span data-stu-id="17fa1-138">NOTES</span></span>

## <span data-ttu-id="17fa1-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17fa1-139">RELATED LINKS</span></span>

[<span data-ttu-id="17fa1-140">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="17fa1-140">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="17fa1-141">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="17fa1-141">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="17fa1-142">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="17fa1-142">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

