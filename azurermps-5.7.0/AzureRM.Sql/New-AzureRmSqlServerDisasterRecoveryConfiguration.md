---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 1fb3f802971f6724545c7006ed67ff01da4d7842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517887"
---
# <span data-ttu-id="30db8-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="30db8-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="30db8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30db8-102">SYNOPSIS</span></span>
<span data-ttu-id="30db8-103">Crea una configurazione di ripristino di sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="30db8-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30db8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30db8-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30db8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30db8-105">DESCRIPTION</span></span>
<span data-ttu-id="30db8-106">Il cmdlet **New-AzureRmSqlServerDisasterRecoveryConfiguration** crea una configurazione di ripristino di sistema di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="30db8-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="30db8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30db8-107">EXAMPLES</span></span>

## <span data-ttu-id="30db8-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30db8-108">PARAMETERS</span></span>

### <span data-ttu-id="30db8-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30db8-109">-AsJob</span></span>
<span data-ttu-id="30db8-110">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="30db8-110">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30db8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30db8-111">-DefaultProfile</span></span>
<span data-ttu-id="30db8-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="30db8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30db8-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="30db8-113">-FailoverPolicy</span></span>
<span data-ttu-id="30db8-114">Specifica i criteri di failover.</span><span class="sxs-lookup"><span data-stu-id="30db8-114">Specifies the failover policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30db8-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30db8-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="30db8-116">Specifica il nome del gruppo di risorse partner.</span><span class="sxs-lookup"><span data-stu-id="30db8-116">Specifies the name of the partner resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30db8-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="30db8-117">-PartnerServerName</span></span>
<span data-ttu-id="30db8-118">Specifica il nome del server partner.</span><span class="sxs-lookup"><span data-stu-id="30db8-118">Specifies the name of the partner server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30db8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30db8-119">-ResourceGroupName</span></span>
<span data-ttu-id="30db8-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30db8-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30db8-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="30db8-121">-ServerName</span></span>
<span data-ttu-id="30db8-122">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="30db8-122">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30db8-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="30db8-123">-VirtualEndpointName</span></span>
<span data-ttu-id="30db8-124">Specifica il nome del punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="30db8-124">Specifies the name of the virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30db8-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30db8-125">-Confirm</span></span>
<span data-ttu-id="30db8-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30db8-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30db8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30db8-127">-WhatIf</span></span>
<span data-ttu-id="30db8-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30db8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30db8-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30db8-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30db8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30db8-130">CommonParameters</span></span>
<span data-ttu-id="30db8-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30db8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30db8-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30db8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30db8-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30db8-133">INPUTS</span></span>

### <span data-ttu-id="30db8-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="30db8-134">None</span></span>
<span data-ttu-id="30db8-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="30db8-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30db8-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30db8-136">OUTPUTS</span></span>

## <span data-ttu-id="30db8-137">Note</span><span class="sxs-lookup"><span data-stu-id="30db8-137">NOTES</span></span>

## <span data-ttu-id="30db8-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30db8-138">RELATED LINKS</span></span>

[<span data-ttu-id="30db8-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="30db8-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="30db8-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="30db8-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="30db8-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="30db8-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="30db8-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="30db8-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
