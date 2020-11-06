---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
ms.openlocfilehash: c378f6315f66b7149c1a8bb6d51ce806425065a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513424"
---
# <span data-ttu-id="db872-101">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="db872-101">Remove-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="db872-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db872-102">SYNOPSIS</span></span>
<span data-ttu-id="db872-103">Cmdlet elimina la configurazione di migrazione per gli spazi dei nomi premium standard</span><span class="sxs-lookup"><span data-stu-id="db872-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db872-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db872-104">SYNTAX</span></span>

### <span data-ttu-id="db872-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db872-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db872-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="db872-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db872-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db872-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db872-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db872-108">DESCRIPTION</span></span>
<span data-ttu-id="db872-109">Il cmdlet **Remove-AzureRmServiceBusMigration** Elimina la configurazione di migrazione per gli spazi dei nomi premium standard</span><span class="sxs-lookup"><span data-stu-id="db872-109">The **Remove-AzureRmServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="db872-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db872-110">EXAMPLES</span></span>

### <span data-ttu-id="db872-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db872-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="db872-112">Elimina la configurazione di migrazione "TestingNamespaceStandardMirgation"</span><span class="sxs-lookup"><span data-stu-id="db872-112">Deletes the 'TestingNamespaceStandardMirgation' migration configuration</span></span>

## <span data-ttu-id="db872-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db872-113">PARAMETERS</span></span>

### <span data-ttu-id="db872-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db872-114">-AsJob</span></span>
<span data-ttu-id="db872-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="db872-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db872-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db872-116">-DefaultProfile</span></span>
<span data-ttu-id="db872-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db872-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db872-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db872-118">-InputObject</span></span>
<span data-ttu-id="db872-119">Oggetto spazio dei nomi standard di migrazione Service Bus</span><span class="sxs-lookup"><span data-stu-id="db872-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="db872-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="db872-120">-Name</span></span>
<span data-ttu-id="db872-121">Nome dello spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="db872-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="db872-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db872-122">-PassThru</span></span>
<span data-ttu-id="db872-123">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="db872-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="db872-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db872-124">-ResourceGroupName</span></span>
<span data-ttu-id="db872-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="db872-125">Resource Group Name</span></span>

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

### <span data-ttu-id="db872-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db872-126">-ResourceId</span></span>
<span data-ttu-id="db872-127">ID risorsa dello spazio dei nomi standard di migrazione Service Bus</span><span class="sxs-lookup"><span data-stu-id="db872-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="db872-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db872-128">-Confirm</span></span>
<span data-ttu-id="db872-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db872-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db872-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db872-130">-WhatIf</span></span>
<span data-ttu-id="db872-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db872-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db872-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db872-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db872-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db872-133">CommonParameters</span></span>
<span data-ttu-id="db872-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db872-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db872-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db872-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db872-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db872-136">INPUTS</span></span>

### <span data-ttu-id="db872-137">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="db872-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="db872-138">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db872-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="db872-139">System. String</span><span class="sxs-lookup"><span data-stu-id="db872-139">System.String</span></span>

## <span data-ttu-id="db872-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db872-140">OUTPUTS</span></span>

### <span data-ttu-id="db872-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db872-141">System.Boolean</span></span>

## <span data-ttu-id="db872-142">Note</span><span class="sxs-lookup"><span data-stu-id="db872-142">NOTES</span></span>

## <span data-ttu-id="db872-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db872-143">RELATED LINKS</span></span>
