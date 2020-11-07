---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: b3978bcc0e3b883d95c5161ca1b24f9cd6c6c1f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674719"
---
# <span data-ttu-id="54bdc-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="54bdc-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="54bdc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="54bdc-103">Crea una nuova istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="54bdc-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="54bdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54bdc-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54bdc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54bdc-105">DESCRIPTION</span></span>
<span data-ttu-id="54bdc-106">Il cmdlet New-AzDataMigrationService crea una nuova istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="54bdc-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="54bdc-107">Questo cmdlet accetta il nome del gruppo di risorse Azure esistente, il nome univoco per la nuova istanza del servizio di migrazione del database di Azure da creare, l'area in cui viene eseguito il provisioning dell'istanza, il nome del codice di lavoro DMS e il nome della subnet virtuale di Azure in cui il servizio deve risiedere.</span><span class="sxs-lookup"><span data-stu-id="54bdc-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="54bdc-108">Non esiste alcun parametro per il nome dell'abbonamento, perché è previsto che l'utente specifichi l'abbonamento predefinito della sessione di accesso di Azure o esegua Get-AzSubscription-Subscriptionname "abbonamento" | Select-AzSubscription per selezionare un altro abbonamento.</span><span class="sxs-lookup"><span data-stu-id="54bdc-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="54bdc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54bdc-109">EXAMPLES</span></span>

### <span data-ttu-id="54bdc-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="54bdc-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="54bdc-111">Nell'esempio precedente viene illustrato come creare una nuova istanza del servizio di migrazione del database di Azure denominata TestService nell'area centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="54bdc-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="54bdc-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54bdc-112">PARAMETERS</span></span>

### <span data-ttu-id="54bdc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54bdc-113">-DefaultProfile</span></span>
<span data-ttu-id="54bdc-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54bdc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54bdc-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="54bdc-115">-Location</span></span>
<span data-ttu-id="54bdc-116">Posizione dell'istanza del servizio di migrazione del database di Azure da creare, che corrisponde a un'area di Azure.</span><span class="sxs-lookup"><span data-stu-id="54bdc-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="54bdc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="54bdc-117">-Name</span></span>
<span data-ttu-id="54bdc-118">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="54bdc-118">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54bdc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54bdc-119">-ResourceGroupName</span></span>
<span data-ttu-id="54bdc-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="54bdc-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="54bdc-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="54bdc-121">-Sku</span></span>
<span data-ttu-id="54bdc-122">SKU per l'istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="54bdc-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="54bdc-123">I valori possibili attualmente sono Basic_1vCore, Basic_2vCores, GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="54bdc-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="54bdc-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="54bdc-124">-VirtualSubnetId</span></span>
<span data-ttu-id="54bdc-125">Nome della subnet nella rete virtuale specificata da usare per l'istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="54bdc-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="54bdc-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="54bdc-126">-Confirm</span></span>
<span data-ttu-id="54bdc-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54bdc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54bdc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54bdc-128">-WhatIf</span></span>
<span data-ttu-id="54bdc-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54bdc-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54bdc-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54bdc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54bdc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54bdc-131">CommonParameters</span></span>
<span data-ttu-id="54bdc-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54bdc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54bdc-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54bdc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54bdc-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54bdc-134">INPUTS</span></span>

### <span data-ttu-id="54bdc-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="54bdc-135">None</span></span>

## <span data-ttu-id="54bdc-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54bdc-136">OUTPUTS</span></span>

### <span data-ttu-id="54bdc-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="54bdc-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="54bdc-138">Note</span><span class="sxs-lookup"><span data-stu-id="54bdc-138">NOTES</span></span>

## <span data-ttu-id="54bdc-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54bdc-139">RELATED LINKS</span></span>
