---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: 615a09d735867d45f9db75ce229d39bc8d9bf75b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031055"
---
# <span data-ttu-id="72ee8-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="72ee8-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="72ee8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="72ee8-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="72ee8-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="72ee8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72ee8-104">SYNTAX</span></span>

### <span data-ttu-id="72ee8-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72ee8-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72ee8-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="72ee8-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72ee8-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72ee8-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72ee8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72ee8-108">DESCRIPTION</span></span>
<span data-ttu-id="72ee8-109">I cmdlet **Stop-AzServiceBusMigration** terminano la migrazione tra lo spazio dei nomi standard e Premium</span><span class="sxs-lookup"><span data-stu-id="72ee8-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="72ee8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72ee8-110">EXAMPLES</span></span>

### <span data-ttu-id="72ee8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="72ee8-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="72ee8-112">Cmdlet termina la migrazione tra spazio dei nomi standard e spazio dei nomi premium disponibile durante la creazione della configurazione della migrazione.</span><span class="sxs-lookup"><span data-stu-id="72ee8-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="72ee8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72ee8-113">PARAMETERS</span></span>

### <span data-ttu-id="72ee8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ee8-114">-DefaultProfile</span></span>
<span data-ttu-id="72ee8-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72ee8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72ee8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72ee8-116">-InputObject</span></span>
<span data-ttu-id="72ee8-117">Oggetto spazio dei nomi standard della configurazione della migrazione di Service Bus</span><span class="sxs-lookup"><span data-stu-id="72ee8-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="72ee8-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="72ee8-118">-Name</span></span>
<span data-ttu-id="72ee8-119">Nome dello spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="72ee8-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="72ee8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72ee8-120">-PassThru</span></span>
<span data-ttu-id="72ee8-121">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="72ee8-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="72ee8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72ee8-122">-ResourceGroupName</span></span>
<span data-ttu-id="72ee8-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="72ee8-123">Resource Group Name</span></span>

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

### <span data-ttu-id="72ee8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72ee8-124">-ResourceId</span></span>
<span data-ttu-id="72ee8-125">ID risorsa dello spazio dei nomi standard della configurazione della migrazione Service Bus</span><span class="sxs-lookup"><span data-stu-id="72ee8-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="72ee8-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72ee8-126">-Confirm</span></span>
<span data-ttu-id="72ee8-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72ee8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72ee8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72ee8-128">-WhatIf</span></span>
<span data-ttu-id="72ee8-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72ee8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72ee8-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72ee8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72ee8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ee8-131">CommonParameters</span></span>
<span data-ttu-id="72ee8-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72ee8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ee8-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72ee8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ee8-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72ee8-134">INPUTS</span></span>

### <span data-ttu-id="72ee8-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="72ee8-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="72ee8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="72ee8-136">System.String</span></span>

## <span data-ttu-id="72ee8-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72ee8-137">OUTPUTS</span></span>

### <span data-ttu-id="72ee8-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72ee8-138">System.Boolean</span></span>

## <span data-ttu-id="72ee8-139">Note</span><span class="sxs-lookup"><span data-stu-id="72ee8-139">NOTES</span></span>

## <span data-ttu-id="72ee8-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72ee8-140">RELATED LINKS</span></span>
