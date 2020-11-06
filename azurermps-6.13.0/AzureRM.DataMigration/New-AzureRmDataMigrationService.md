---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: cc2f708294be05b16b0c5be94fb9da260b479799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518692"
---
# <span data-ttu-id="eafb3-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="eafb3-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="eafb3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eafb3-102">SYNOPSIS</span></span>
<span data-ttu-id="eafb3-103">Crea una nuova istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="eafb3-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eafb3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eafb3-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eafb3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eafb3-105">DESCRIPTION</span></span>
<span data-ttu-id="eafb3-106">Il cmdlet New-AzureRmDataMigrationService crea una nuova istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="eafb3-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="eafb3-107">Questo cmdlet accetta il nome del gruppo di risorse Azure esistente, il nome univoco per la nuova istanza del servizio di migrazione del database di Azure da creare, l'area in cui viene eseguito il provisioning dell'istanza, il nome del codice di lavoro DMS e il nome della subnet virtuale di Azure in cui il servizio deve risiedere.</span><span class="sxs-lookup"><span data-stu-id="eafb3-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="eafb3-108">Non esiste alcun parametro per il nome dell'abbonamento, perché è previsto che l'utente specifichi l'abbonamento predefinito della sessione di accesso di Azure o esegua Get-AzureRmSubscription-Subscriptionname "abbonamento" | Select-AzureRmSubscription per selezionare un altro abbonamento.</span><span class="sxs-lookup"><span data-stu-id="eafb3-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription -SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="eafb3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eafb3-109">EXAMPLES</span></span>

### <span data-ttu-id="eafb3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eafb3-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="eafb3-111">Nell'esempio precedente viene illustrato come creare una nuova istanza del servizio di migrazione del database di Azure denominata TestService nell'area centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="eafb3-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="eafb3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eafb3-112">PARAMETERS</span></span>

### <span data-ttu-id="eafb3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafb3-113">-DefaultProfile</span></span>
<span data-ttu-id="eafb3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eafb3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eafb3-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="eafb3-115">-Location</span></span>
<span data-ttu-id="eafb3-116">Posizione dell'istanza del servizio di migrazione del database di Azure da creare, che corrisponde a un'area di Azure.</span><span class="sxs-lookup"><span data-stu-id="eafb3-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="eafb3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="eafb3-117">-Name</span></span>
<span data-ttu-id="eafb3-118">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="eafb3-118">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="eafb3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eafb3-119">-ResourceGroupName</span></span>
<span data-ttu-id="eafb3-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eafb3-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="eafb3-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="eafb3-121">-Sku</span></span>
<span data-ttu-id="eafb3-122">SKU per l'istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="eafb3-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="eafb3-123">I valori possibili attualmente sono Basic_1vCore, Basic_2vCores, GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="eafb3-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="eafb3-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="eafb3-124">-VirtualSubnetId</span></span>
<span data-ttu-id="eafb3-125">Nome della subnet nella rete virtuale specificata da usare per l'istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="eafb3-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="eafb3-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eafb3-126">-Confirm</span></span>
<span data-ttu-id="eafb3-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eafb3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eafb3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eafb3-128">-WhatIf</span></span>
<span data-ttu-id="eafb3-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eafb3-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eafb3-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eafb3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eafb3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafb3-131">CommonParameters</span></span>
<span data-ttu-id="eafb3-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eafb3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafb3-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eafb3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafb3-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eafb3-134">INPUTS</span></span>

### <span data-ttu-id="eafb3-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eafb3-135">None</span></span>

## <span data-ttu-id="eafb3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eafb3-136">OUTPUTS</span></span>

### <span data-ttu-id="eafb3-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="eafb3-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="eafb3-138">Note</span><span class="sxs-lookup"><span data-stu-id="eafb3-138">NOTES</span></span>

## <span data-ttu-id="eafb3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eafb3-139">RELATED LINKS</span></span>
