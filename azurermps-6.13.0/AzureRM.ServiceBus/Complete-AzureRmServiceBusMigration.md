---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/complete-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
ms.openlocfilehash: 0006e4768dc27994d18e93e48696b5ee9a514c45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687261"
---
# <span data-ttu-id="62364-101">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="62364-101">Complete-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="62364-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62364-102">SYNOPSIS</span></span>
<span data-ttu-id="62364-103">I cmdlet impostano la migrazione dallo spazio dei nomi standard a Premium come stringhe complete e di connessione dello spazio dei nomi standard ora puntano allo spazio dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="62364-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62364-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62364-104">SYNTAX</span></span>

### <span data-ttu-id="62364-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62364-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62364-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62364-106">NamespaceInputObjectSet</span></span>
```
Complete-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62364-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62364-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62364-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62364-108">DESCRIPTION</span></span>
<span data-ttu-id="62364-109">I cmdlet **complete-AzureRmServiceBusMigration** impostano la migrazione dallo spazio dei nomi standard a Premium come le stringhe complete e di connessione dello spazio dei nomi standard ora puntano allo spazio dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="62364-109">The **Complete-AzureRmServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="62364-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62364-110">EXAMPLES</span></span>

### <span data-ttu-id="62364-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="62364-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMirgation
```

<span data-ttu-id="62364-112">Imposta la migrazione dello spazio dei nomi "NamespaceStandardMirgation" come completata.</span><span class="sxs-lookup"><span data-stu-id="62364-112">Sets the Migration of 'NamespaceStandardMirgation' namespace as complete.</span></span>

## <span data-ttu-id="62364-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62364-113">PARAMETERS</span></span>

### <span data-ttu-id="62364-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62364-114">-DefaultProfile</span></span>
<span data-ttu-id="62364-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62364-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62364-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62364-116">-InputObject</span></span>
<span data-ttu-id="62364-117">Configurazione della migrazione di Service Bus-oggetto standard dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="62364-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62364-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="62364-118">-Name</span></span>
<span data-ttu-id="62364-119">Nome dello spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="62364-119">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62364-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62364-120">-PassThru</span></span>
<span data-ttu-id="62364-121">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="62364-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="62364-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62364-122">-ResourceGroupName</span></span>
<span data-ttu-id="62364-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="62364-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62364-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62364-124">-ResourceId</span></span>
<span data-ttu-id="62364-125">Service Bus migratio-ID risorsa standard dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="62364-125">Service Bus Migratio - Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62364-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62364-126">-Confirm</span></span>
<span data-ttu-id="62364-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62364-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62364-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62364-128">-WhatIf</span></span>
<span data-ttu-id="62364-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62364-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62364-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62364-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62364-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62364-131">CommonParameters</span></span>
<span data-ttu-id="62364-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62364-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62364-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62364-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62364-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62364-134">INPUTS</span></span>

### <span data-ttu-id="62364-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="62364-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="62364-136">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="62364-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="62364-137">System. String</span><span class="sxs-lookup"><span data-stu-id="62364-137">System.String</span></span>

## <span data-ttu-id="62364-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62364-138">OUTPUTS</span></span>

### <span data-ttu-id="62364-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62364-139">System.Boolean</span></span>

## <span data-ttu-id="62364-140">Note</span><span class="sxs-lookup"><span data-stu-id="62364-140">NOTES</span></span>

## <span data-ttu-id="62364-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62364-141">RELATED LINKS</span></span>
