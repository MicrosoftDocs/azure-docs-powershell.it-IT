---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 99892ee748de030a045bd9d0a022051206236198
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688503"
---
# <span data-ttu-id="723cd-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="723cd-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="723cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="723cd-102">SYNOPSIS</span></span>
<span data-ttu-id="723cd-103">Rimuove un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="723cd-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="723cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="723cd-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="723cd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="723cd-105">DESCRIPTION</span></span>
<span data-ttu-id="723cd-106">Il cmdlet **Remove-AzureRmSqlSyncGroup** rimuove un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="723cd-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="723cd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="723cd-107">EXAMPLES</span></span>

### <span data-ttu-id="723cd-108">Esempio 1: rimuovere un gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="723cd-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="723cd-109">Questo comando rimuove il gruppo di sincronizzazione di database SQL di Azure denominato syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="723cd-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="723cd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="723cd-110">PARAMETERS</span></span>

### <span data-ttu-id="723cd-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="723cd-111">-Confirm</span></span>
<span data-ttu-id="723cd-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="723cd-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="723cd-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="723cd-113">-DatabaseName</span></span>
<span data-ttu-id="723cd-114">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="723cd-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="723cd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="723cd-115">-Force</span></span>
<span data-ttu-id="723cd-116">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="723cd-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="723cd-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="723cd-117">-Name</span></span>
<span data-ttu-id="723cd-118">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="723cd-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="723cd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="723cd-119">-PassThru</span></span>
<span data-ttu-id="723cd-120">Definisce se restituire il gruppo di sincronizzazione rimosso</span><span class="sxs-lookup"><span data-stu-id="723cd-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="723cd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="723cd-121">-ResourceGroupName</span></span>
<span data-ttu-id="723cd-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="723cd-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="723cd-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="723cd-123">-ServerName</span></span>
<span data-ttu-id="723cd-124">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="723cd-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="723cd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="723cd-125">-WhatIf</span></span>
<span data-ttu-id="723cd-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="723cd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="723cd-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="723cd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="723cd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="723cd-128">-DefaultProfile</span></span>
<span data-ttu-id="723cd-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="723cd-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="723cd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="723cd-130">CommonParameters</span></span>
<span data-ttu-id="723cd-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="723cd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="723cd-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="723cd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="723cd-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="723cd-133">INPUTS</span></span>

## <span data-ttu-id="723cd-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="723cd-134">OUTPUTS</span></span>

### <span data-ttu-id="723cd-135">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="723cd-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="723cd-136">Note</span><span class="sxs-lookup"><span data-stu-id="723cd-136">NOTES</span></span>

## <span data-ttu-id="723cd-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="723cd-137">RELATED LINKS</span></span>

[<span data-ttu-id="723cd-138">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="723cd-138">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="723cd-139">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="723cd-139">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="723cd-140">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="723cd-140">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

