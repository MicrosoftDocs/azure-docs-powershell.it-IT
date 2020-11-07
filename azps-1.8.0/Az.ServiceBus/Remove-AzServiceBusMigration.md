---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: eff58056393c499e15a7ddb4ab018b7ff6e383a5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677125"
---
# <span data-ttu-id="c3329-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c3329-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="c3329-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3329-102">SYNOPSIS</span></span>
<span data-ttu-id="c3329-103">Cmdlet elimina la configurazione di migrazione per gli spazi dei nomi premium standard</span><span class="sxs-lookup"><span data-stu-id="c3329-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="c3329-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3329-104">SYNTAX</span></span>

### <span data-ttu-id="c3329-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c3329-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3329-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c3329-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3329-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3329-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3329-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3329-108">DESCRIPTION</span></span>
<span data-ttu-id="c3329-109">Il cmdlet **Remove-AzServiceBusMigration** Elimina la configurazione di migrazione per gli spazi dei nomi premium standard</span><span class="sxs-lookup"><span data-stu-id="c3329-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="c3329-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3329-110">EXAMPLES</span></span>

### <span data-ttu-id="c3329-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c3329-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="c3329-112">Elimina la configurazione di migrazione "TestingNamespaceStandardMirgation"</span><span class="sxs-lookup"><span data-stu-id="c3329-112">Deletes the 'TestingNamespaceStandardMirgation' migration configuration</span></span>

## <span data-ttu-id="c3329-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3329-113">PARAMETERS</span></span>

### <span data-ttu-id="c3329-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3329-114">-AsJob</span></span>
<span data-ttu-id="c3329-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c3329-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3329-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3329-116">-DefaultProfile</span></span>
<span data-ttu-id="c3329-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3329-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3329-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3329-118">-InputObject</span></span>
<span data-ttu-id="c3329-119">Oggetto spazio dei nomi standard di migrazione Service Bus</span><span class="sxs-lookup"><span data-stu-id="c3329-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="c3329-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3329-120">-Name</span></span>
<span data-ttu-id="c3329-121">Nome dello spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="c3329-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="c3329-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3329-122">-PassThru</span></span>
<span data-ttu-id="c3329-123">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="c3329-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c3329-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3329-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3329-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c3329-125">Resource Group Name</span></span>

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

### <span data-ttu-id="c3329-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3329-126">-ResourceId</span></span>
<span data-ttu-id="c3329-127">ID risorsa dello spazio dei nomi standard di migrazione Service Bus</span><span class="sxs-lookup"><span data-stu-id="c3329-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="c3329-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c3329-128">-Confirm</span></span>
<span data-ttu-id="c3329-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3329-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3329-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3329-130">-WhatIf</span></span>
<span data-ttu-id="c3329-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3329-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3329-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3329-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3329-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3329-133">CommonParameters</span></span>
<span data-ttu-id="c3329-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3329-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3329-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3329-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3329-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3329-136">INPUTS</span></span>

### <span data-ttu-id="c3329-137">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c3329-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="c3329-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c3329-138">System.String</span></span>

## <span data-ttu-id="c3329-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3329-139">OUTPUTS</span></span>

### <span data-ttu-id="c3329-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3329-140">System.Boolean</span></span>

## <span data-ttu-id="c3329-141">Note</span><span class="sxs-lookup"><span data-stu-id="c3329-141">NOTES</span></span>

## <span data-ttu-id="c3329-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3329-142">RELATED LINKS</span></span>