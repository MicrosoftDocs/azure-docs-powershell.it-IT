---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190111"
---
# <span data-ttu-id="106d9-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="106d9-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="106d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="106d9-102">SYNOPSIS</span></span>
<span data-ttu-id="106d9-103">Cmdlet elimina la configurazione di migrazione per gli spazi dei nomi premium standard</span><span class="sxs-lookup"><span data-stu-id="106d9-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="106d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="106d9-104">SYNTAX</span></span>

### <span data-ttu-id="106d9-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="106d9-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="106d9-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="106d9-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="106d9-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="106d9-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="106d9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="106d9-108">DESCRIPTION</span></span>
<span data-ttu-id="106d9-109">Il cmdlet **Remove-AzServiceBusMigration** Elimina la configurazione di migrazione per gli spazi dei nomi premium standard</span><span class="sxs-lookup"><span data-stu-id="106d9-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="106d9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="106d9-110">EXAMPLES</span></span>

### <span data-ttu-id="106d9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="106d9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="106d9-112">Elimina la configurazione di migrazione "TestingNamespaceStandardMigration"</span><span class="sxs-lookup"><span data-stu-id="106d9-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="106d9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="106d9-113">PARAMETERS</span></span>

### <span data-ttu-id="106d9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="106d9-114">-AsJob</span></span>
<span data-ttu-id="106d9-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="106d9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="106d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="106d9-116">-DefaultProfile</span></span>
<span data-ttu-id="106d9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="106d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="106d9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="106d9-118">-InputObject</span></span>
<span data-ttu-id="106d9-119">Oggetto spazio dei nomi standard di migrazione Service Bus</span><span class="sxs-lookup"><span data-stu-id="106d9-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="106d9-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="106d9-120">-Name</span></span>
<span data-ttu-id="106d9-121">Nome dello spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="106d9-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="106d9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="106d9-122">-PassThru</span></span>
<span data-ttu-id="106d9-123">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="106d9-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="106d9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="106d9-124">-ResourceGroupName</span></span>
<span data-ttu-id="106d9-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="106d9-125">Resource Group Name</span></span>

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

### <span data-ttu-id="106d9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="106d9-126">-ResourceId</span></span>
<span data-ttu-id="106d9-127">ID risorsa dello spazio dei nomi standard di migrazione Service Bus</span><span class="sxs-lookup"><span data-stu-id="106d9-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="106d9-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="106d9-128">-Confirm</span></span>
<span data-ttu-id="106d9-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="106d9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="106d9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="106d9-130">-WhatIf</span></span>
<span data-ttu-id="106d9-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="106d9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="106d9-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="106d9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="106d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="106d9-133">CommonParameters</span></span>
<span data-ttu-id="106d9-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="106d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="106d9-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="106d9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="106d9-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="106d9-136">INPUTS</span></span>

### <span data-ttu-id="106d9-137">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="106d9-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="106d9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="106d9-138">System.String</span></span>

## <span data-ttu-id="106d9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="106d9-139">OUTPUTS</span></span>

### <span data-ttu-id="106d9-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="106d9-140">System.Boolean</span></span>

## <span data-ttu-id="106d9-141">Note</span><span class="sxs-lookup"><span data-stu-id="106d9-141">NOTES</span></span>

## <span data-ttu-id="106d9-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="106d9-142">RELATED LINKS</span></span>