---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 508a19b51fea8435ec48e060e63ee3b3cecc5f65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514764"
---
# <span data-ttu-id="88075-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="88075-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="88075-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88075-102">SYNOPSIS</span></span>
<span data-ttu-id="88075-103">Ottiene l'attività per una configurazione di ripristino di sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="88075-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88075-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88075-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88075-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88075-105">DESCRIPTION</span></span>
<span data-ttu-id="88075-106">Il cmdlet **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** ottiene un'attività per una configurazione di ripristino del sistema di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="88075-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="88075-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88075-107">EXAMPLES</span></span>

## <span data-ttu-id="88075-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88075-108">PARAMETERS</span></span>

### <span data-ttu-id="88075-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88075-109">-DefaultProfile</span></span>
<span data-ttu-id="88075-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="88075-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88075-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="88075-111">-OperationId</span></span>
<span data-ttu-id="88075-112">Specifica l'ID operazione.</span><span class="sxs-lookup"><span data-stu-id="88075-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88075-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88075-113">-ResourceGroupName</span></span>
<span data-ttu-id="88075-114">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="88075-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="88075-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="88075-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="88075-116">Specifica il nome della configurazione del ripristino del sistema server.</span><span class="sxs-lookup"><span data-stu-id="88075-116">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88075-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="88075-117">-ServerName</span></span>
<span data-ttu-id="88075-118">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="88075-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="88075-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="88075-119">-Confirm</span></span>
<span data-ttu-id="88075-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88075-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88075-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88075-121">-WhatIf</span></span>
<span data-ttu-id="88075-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88075-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88075-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88075-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88075-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88075-124">CommonParameters</span></span>
<span data-ttu-id="88075-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88075-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88075-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88075-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88075-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88075-127">INPUTS</span></span>

### <span data-ttu-id="88075-128">System. String</span><span class="sxs-lookup"><span data-stu-id="88075-128">System.String</span></span>

### <span data-ttu-id="88075-129">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="88075-129">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="88075-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88075-130">OUTPUTS</span></span>

### <span data-ttu-id="88075-131">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="88075-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="88075-132">Note</span><span class="sxs-lookup"><span data-stu-id="88075-132">NOTES</span></span>

## <span data-ttu-id="88075-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88075-133">RELATED LINKS</span></span>

[<span data-ttu-id="88075-134">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="88075-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
