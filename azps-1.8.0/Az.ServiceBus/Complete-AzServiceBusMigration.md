---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 843ca61427d8aa5c2eea3d91f0dd8e5c22bb847f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677173"
---
# <span data-ttu-id="abb74-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="abb74-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="abb74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="abb74-102">SYNOPSIS</span></span>
<span data-ttu-id="abb74-103">I cmdlet impostano la migrazione dallo spazio dei nomi standard a Premium come stringhe complete e di connessione dello spazio dei nomi standard ora puntano allo spazio dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="abb74-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="abb74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="abb74-104">SYNTAX</span></span>

### <span data-ttu-id="abb74-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="abb74-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abb74-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="abb74-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abb74-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abb74-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abb74-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abb74-108">DESCRIPTION</span></span>
<span data-ttu-id="abb74-109">I cmdlet **complete-AzServiceBusMigration** impostano la migrazione dallo spazio dei nomi standard a Premium come le stringhe complete e di connessione dello spazio dei nomi standard ora puntano allo spazio dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="abb74-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="abb74-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="abb74-110">EXAMPLES</span></span>

### <span data-ttu-id="abb74-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="abb74-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMirgation
```

<span data-ttu-id="abb74-112">Imposta la migrazione dello spazio dei nomi "NamespaceStandardMirgation" come completata.</span><span class="sxs-lookup"><span data-stu-id="abb74-112">Sets the Migration of 'NamespaceStandardMirgation' namespace as complete.</span></span>

## <span data-ttu-id="abb74-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="abb74-113">PARAMETERS</span></span>

### <span data-ttu-id="abb74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb74-114">-DefaultProfile</span></span>
<span data-ttu-id="abb74-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="abb74-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abb74-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abb74-116">-InputObject</span></span>
<span data-ttu-id="abb74-117">Configurazione della migrazione di Service Bus-oggetto standard dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="abb74-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="abb74-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="abb74-118">-Name</span></span>
<span data-ttu-id="abb74-119">Nome dello spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="abb74-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="abb74-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abb74-120">-PassThru</span></span>
<span data-ttu-id="abb74-121">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="abb74-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="abb74-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abb74-122">-ResourceGroupName</span></span>
<span data-ttu-id="abb74-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="abb74-123">Resource Group Name</span></span>

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

### <span data-ttu-id="abb74-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abb74-124">-ResourceId</span></span>
<span data-ttu-id="abb74-125">Service Bus migratio-ID risorsa standard dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="abb74-125">Service Bus Migratio - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="abb74-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="abb74-126">-Confirm</span></span>
<span data-ttu-id="abb74-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abb74-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abb74-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abb74-128">-WhatIf</span></span>
<span data-ttu-id="abb74-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abb74-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abb74-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abb74-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abb74-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb74-131">CommonParameters</span></span>
<span data-ttu-id="abb74-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abb74-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb74-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb74-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb74-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="abb74-134">INPUTS</span></span>

### <span data-ttu-id="abb74-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="abb74-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="abb74-136">System. String</span><span class="sxs-lookup"><span data-stu-id="abb74-136">System.String</span></span>

## <span data-ttu-id="abb74-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="abb74-137">OUTPUTS</span></span>

### <span data-ttu-id="abb74-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="abb74-138">System.Boolean</span></span>

## <span data-ttu-id="abb74-139">Note</span><span class="sxs-lookup"><span data-stu-id="abb74-139">NOTES</span></span>

## <span data-ttu-id="abb74-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="abb74-140">RELATED LINKS</span></span>
