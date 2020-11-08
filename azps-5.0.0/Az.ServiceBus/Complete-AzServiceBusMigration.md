---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 883ecf9337cea2b46166b4c1be8625c9763eb7db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202605"
---
# <span data-ttu-id="935d2-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="935d2-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="935d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="935d2-102">SYNOPSIS</span></span>
<span data-ttu-id="935d2-103">I cmdlet impostano la migrazione dallo spazio dei nomi standard a Premium come stringhe complete e di connessione dello spazio dei nomi standard ora puntano allo spazio dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="935d2-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="935d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="935d2-104">SYNTAX</span></span>

### <span data-ttu-id="935d2-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="935d2-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="935d2-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="935d2-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="935d2-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="935d2-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="935d2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="935d2-108">DESCRIPTION</span></span>
<span data-ttu-id="935d2-109">I cmdlet **complete-AzServiceBusMigration** impostano la migrazione dallo spazio dei nomi standard a Premium come le stringhe complete e di connessione dello spazio dei nomi standard ora puntano allo spazio dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="935d2-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="935d2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="935d2-110">EXAMPLES</span></span>

### <span data-ttu-id="935d2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="935d2-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="935d2-112">Imposta la migrazione dello spazio dei nomi "NamespaceStandardMigration" come completata.</span><span class="sxs-lookup"><span data-stu-id="935d2-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="935d2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="935d2-113">PARAMETERS</span></span>

### <span data-ttu-id="935d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935d2-114">-DefaultProfile</span></span>
<span data-ttu-id="935d2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="935d2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="935d2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="935d2-116">-InputObject</span></span>
<span data-ttu-id="935d2-117">Configurazione della migrazione di Service Bus-oggetto standard dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="935d2-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="935d2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="935d2-118">-Name</span></span>
<span data-ttu-id="935d2-119">Nome dello spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="935d2-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="935d2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="935d2-120">-PassThru</span></span>
<span data-ttu-id="935d2-121">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="935d2-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="935d2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="935d2-122">-ResourceGroupName</span></span>
<span data-ttu-id="935d2-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="935d2-123">Resource Group Name</span></span>

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

### <span data-ttu-id="935d2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="935d2-124">-ResourceId</span></span>
<span data-ttu-id="935d2-125">Migrazione di Service Bus-ID standard delle risorse dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="935d2-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="935d2-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="935d2-126">-Confirm</span></span>
<span data-ttu-id="935d2-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="935d2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="935d2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="935d2-128">-WhatIf</span></span>
<span data-ttu-id="935d2-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="935d2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="935d2-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="935d2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="935d2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935d2-131">CommonParameters</span></span>
<span data-ttu-id="935d2-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="935d2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935d2-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="935d2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935d2-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="935d2-134">INPUTS</span></span>

### <span data-ttu-id="935d2-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="935d2-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="935d2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="935d2-136">System.String</span></span>

## <span data-ttu-id="935d2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="935d2-137">OUTPUTS</span></span>

### <span data-ttu-id="935d2-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="935d2-138">System.Boolean</span></span>

## <span data-ttu-id="935d2-139">Note</span><span class="sxs-lookup"><span data-stu-id="935d2-139">NOTES</span></span>

## <span data-ttu-id="935d2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="935d2-140">RELATED LINKS</span></span>
