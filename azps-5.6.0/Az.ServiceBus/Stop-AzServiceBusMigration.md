---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: fc0cc8acf45403593124135cab87072a719f291d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961598"
---
# <span data-ttu-id="2eac5-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2eac5-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="2eac5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eac5-102">SYNOPSIS</span></span>
<span data-ttu-id="2eac5-103">{{Fill in the Synopsis}}</span><span class="sxs-lookup"><span data-stu-id="2eac5-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="2eac5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2eac5-104">SYNTAX</span></span>

### <span data-ttu-id="2eac5-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2eac5-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eac5-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2eac5-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eac5-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2eac5-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eac5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2eac5-108">DESCRIPTION</span></span>
<span data-ttu-id="2eac5-109">Il cmdlet **Stop-AzServiceBusMigration** termina la migrazione tra lo spazio dei nomi Standard e Premium</span><span class="sxs-lookup"><span data-stu-id="2eac5-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="2eac5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2eac5-110">EXAMPLES</span></span>

### <span data-ttu-id="2eac5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2eac5-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="2eac5-112">Il cmdlet termina la migrazione tra lo spazio dei nomi Standard e lo spazio dei nomi Premium fornito durante la creazione della configurazione di migrazione.</span><span class="sxs-lookup"><span data-stu-id="2eac5-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="2eac5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eac5-113">PARAMETERS</span></span>

### <span data-ttu-id="2eac5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eac5-114">-DefaultProfile</span></span>
<span data-ttu-id="2eac5-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2eac5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eac5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eac5-116">-InputObject</span></span>
<span data-ttu-id="2eac5-117">Oggetto spazio dei nomi standard di configurazione del bus di servizio</span><span class="sxs-lookup"><span data-stu-id="2eac5-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="2eac5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2eac5-118">-Name</span></span>
<span data-ttu-id="2eac5-119">Nome spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="2eac5-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="2eac5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2eac5-120">-PassThru</span></span>
<span data-ttu-id="2eac5-121">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2eac5-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2eac5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eac5-122">-ResourceGroupName</span></span>
<span data-ttu-id="2eac5-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2eac5-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eac5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2eac5-124">-ResourceId</span></span>
<span data-ttu-id="2eac5-125">ID risorsa spazio dei nomi standard di configurazione bus di servizio</span><span class="sxs-lookup"><span data-stu-id="2eac5-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="2eac5-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2eac5-126">-Confirm</span></span>
<span data-ttu-id="2eac5-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eac5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eac5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eac5-128">-WhatIf</span></span>
<span data-ttu-id="2eac5-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2eac5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eac5-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2eac5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eac5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eac5-131">CommonParameters</span></span>
<span data-ttu-id="2eac5-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eac5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eac5-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eac5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eac5-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="2eac5-134">INPUTS</span></span>

### <span data-ttu-id="2eac5-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2eac5-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="2eac5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2eac5-136">System.String</span></span>

## <span data-ttu-id="2eac5-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2eac5-137">OUTPUTS</span></span>

### <span data-ttu-id="2eac5-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2eac5-138">System.Boolean</span></span>

## <span data-ttu-id="2eac5-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="2eac5-139">NOTES</span></span>

## <span data-ttu-id="2eac5-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2eac5-140">RELATED LINKS</span></span>
