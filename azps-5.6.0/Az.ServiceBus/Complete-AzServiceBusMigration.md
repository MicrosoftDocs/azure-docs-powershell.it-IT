---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 3d993e95eb3a92e5b0894e020af06d2d88b8ed4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011645"
---
# <span data-ttu-id="ebe2a-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ebe2a-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="ebe2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebe2a-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe2a-103">I cmdlet impostano la migrazione dallo spazio dei nomi Standard a Premium come stringhe di connessione complete dello spazio dei nomi standard ora puntano allo spazio dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="ebe2a-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="ebe2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ebe2a-104">SYNTAX</span></span>

### <span data-ttu-id="ebe2a-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ebe2a-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe2a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ebe2a-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe2a-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebe2a-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebe2a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ebe2a-108">DESCRIPTION</span></span>
<span data-ttu-id="ebe2a-109">I cmdlet **Complete-AzServiceBusMigration** impostano la migrazione da Standard a spazio dei nomi Premium come stringhe complete e le stringhe di connessione dello spazio dei nomi standard ora puntano allo spazio dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="ebe2a-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="ebe2a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ebe2a-110">EXAMPLES</span></span>

### <span data-ttu-id="ebe2a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ebe2a-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="ebe2a-112">Imposta la migrazione dello spazio dei nomi 'NamespaceStandardMigration' come completata.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="ebe2a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebe2a-113">PARAMETERS</span></span>

### <span data-ttu-id="ebe2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe2a-114">-DefaultProfile</span></span>
<span data-ttu-id="ebe2a-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebe2a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebe2a-116">-InputObject</span></span>
<span data-ttu-id="ebe2a-117">Configurazione della migrazione del bus di servizio - Oggetto Spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="ebe2a-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="ebe2a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ebe2a-118">-Name</span></span>
<span data-ttu-id="ebe2a-119">Nome spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="ebe2a-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="ebe2a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebe2a-120">-PassThru</span></span>
<span data-ttu-id="ebe2a-121">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ebe2a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebe2a-122">-ResourceGroupName</span></span>
<span data-ttu-id="ebe2a-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ebe2a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ebe2a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebe2a-124">-ResourceId</span></span>
<span data-ttu-id="ebe2a-125">Migrazione bus di servizio - ID risorsa spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="ebe2a-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="ebe2a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebe2a-126">-Confirm</span></span>
<span data-ttu-id="ebe2a-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebe2a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebe2a-128">-WhatIf</span></span>
<span data-ttu-id="ebe2a-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebe2a-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebe2a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe2a-131">CommonParameters</span></span>
<span data-ttu-id="ebe2a-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe2a-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebe2a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe2a-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="ebe2a-134">INPUTS</span></span>

### <span data-ttu-id="ebe2a-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ebe2a-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="ebe2a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ebe2a-136">System.String</span></span>

## <span data-ttu-id="ebe2a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ebe2a-137">OUTPUTS</span></span>

### <span data-ttu-id="ebe2a-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ebe2a-138">System.Boolean</span></span>

## <span data-ttu-id="ebe2a-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="ebe2a-139">NOTES</span></span>

## <span data-ttu-id="ebe2a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ebe2a-140">RELATED LINKS</span></span>
