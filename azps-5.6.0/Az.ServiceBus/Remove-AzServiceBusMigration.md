---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 9e53dab771486758cbd57c8f5c530a458df655d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950942"
---
# <span data-ttu-id="8be93-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8be93-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="8be93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8be93-102">SYNOPSIS</span></span>
<span data-ttu-id="8be93-103">Il cmdlet elimina la configurazione della migrazione per gli spazi dei nomi Da Standard a Premium</span><span class="sxs-lookup"><span data-stu-id="8be93-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="8be93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8be93-104">SYNTAX</span></span>

### <span data-ttu-id="8be93-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8be93-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8be93-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8be93-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8be93-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8be93-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8be93-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8be93-108">DESCRIPTION</span></span>
<span data-ttu-id="8be93-109">Il cmdlet **Remove-AzServiceBusMigration** elimina la configurazione della migrazione per gli spazi dei nomi Da Standard a Premium</span><span class="sxs-lookup"><span data-stu-id="8be93-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="8be93-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8be93-110">EXAMPLES</span></span>

### <span data-ttu-id="8be93-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8be93-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="8be93-112">Elimina la configurazione di migrazione 'TestingStandardMigration'</span><span class="sxs-lookup"><span data-stu-id="8be93-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="8be93-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8be93-113">PARAMETERS</span></span>

### <span data-ttu-id="8be93-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8be93-114">-AsJob</span></span>
<span data-ttu-id="8be93-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8be93-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8be93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be93-116">-DefaultProfile</span></span>
<span data-ttu-id="8be93-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8be93-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8be93-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8be93-118">-InputObject</span></span>
<span data-ttu-id="8be93-119">Oggetto Spazio dei nomi standard di migrazione del bus di servizio</span><span class="sxs-lookup"><span data-stu-id="8be93-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="8be93-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8be93-120">-Name</span></span>
<span data-ttu-id="8be93-121">Nome spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="8be93-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="8be93-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8be93-122">-PassThru</span></span>
<span data-ttu-id="8be93-123">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8be93-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8be93-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be93-124">-ResourceGroupName</span></span>
<span data-ttu-id="8be93-125">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8be93-125">Resource Group Name</span></span>

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

### <span data-ttu-id="8be93-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8be93-126">-ResourceId</span></span>
<span data-ttu-id="8be93-127">ID risorsa spazio dei nomi standard di migrazione bus di servizio</span><span class="sxs-lookup"><span data-stu-id="8be93-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="8be93-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8be93-128">-Confirm</span></span>
<span data-ttu-id="8be93-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8be93-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8be93-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8be93-130">-WhatIf</span></span>
<span data-ttu-id="8be93-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8be93-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8be93-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8be93-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8be93-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be93-133">CommonParameters</span></span>
<span data-ttu-id="8be93-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be93-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be93-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be93-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be93-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="8be93-136">INPUTS</span></span>

### <span data-ttu-id="8be93-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="8be93-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="8be93-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8be93-138">System.String</span></span>

## <span data-ttu-id="8be93-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8be93-139">OUTPUTS</span></span>

### <span data-ttu-id="8be93-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8be93-140">System.Boolean</span></span>

## <span data-ttu-id="8be93-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="8be93-141">NOTES</span></span>

## <span data-ttu-id="8be93-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8be93-142">RELATED LINKS</span></span>
