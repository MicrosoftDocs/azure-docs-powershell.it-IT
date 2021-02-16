---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: db6d94b4aa2f6182abc114f11d1dba0b40ebbb93
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183438"
---
# <span data-ttu-id="50d69-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="50d69-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="50d69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50d69-102">SYNOPSIS</span></span>
<span data-ttu-id="50d69-103">Rimuovere una o più impostazioni di Tessuto di servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="50d69-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="50d69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50d69-104">SYNTAX</span></span>

### <span data-ttu-id="50d69-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="50d69-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d69-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="50d69-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50d69-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="50d69-107">DESCRIPTION</span></span>
<span data-ttu-id="50d69-108">Usare **Remove-AzServiceFabricSetting** per rimuovere le impostazioni di Service Fabric dal cluster.</span><span class="sxs-lookup"><span data-stu-id="50d69-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="50d69-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50d69-109">EXAMPLES</span></span>

### <span data-ttu-id="50d69-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50d69-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="50d69-111">Questo comando rimuove le impostazioni 'MaxCursors' nella sezione 'EseStore'.</span><span class="sxs-lookup"><span data-stu-id="50d69-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="50d69-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50d69-112">PARAMETERS</span></span>

### <span data-ttu-id="50d69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d69-113">-DefaultProfile</span></span>
<span data-ttu-id="50d69-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50d69-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50d69-115">-Name</span><span class="sxs-lookup"><span data-stu-id="50d69-115">-Name</span></span>
<span data-ttu-id="50d69-116">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="50d69-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50d69-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="50d69-117">-Parameter</span></span>
<span data-ttu-id="50d69-118">Nome parametro dell'impostazione tessuto</span><span class="sxs-lookup"><span data-stu-id="50d69-118">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50d69-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50d69-119">-ResourceGroupName</span></span>
<span data-ttu-id="50d69-120">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50d69-120">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50d69-121">-Section</span><span class="sxs-lookup"><span data-stu-id="50d69-121">-Section</span></span>
<span data-ttu-id="50d69-122">Nome della sezione dell'impostazione del tessuto</span><span class="sxs-lookup"><span data-stu-id="50d69-122">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50d69-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="50d69-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="50d69-124">Una serie di impostazioni dei tessuto</span><span class="sxs-lookup"><span data-stu-id="50d69-124">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50d69-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50d69-125">-Confirm</span></span>
<span data-ttu-id="50d69-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50d69-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50d69-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50d69-127">-WhatIf</span></span>
<span data-ttu-id="50d69-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50d69-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50d69-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50d69-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50d69-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d69-130">CommonParameters</span></span>
<span data-ttu-id="50d69-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50d69-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d69-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="50d69-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d69-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="50d69-133">INPUTS</span></span>

### <span data-ttu-id="50d69-134">System.String</span><span class="sxs-lookup"><span data-stu-id="50d69-134">System.String</span></span>

### <span data-ttu-id="50d69-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="50d69-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="50d69-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50d69-136">OUTPUTS</span></span>

### <span data-ttu-id="50d69-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="50d69-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="50d69-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="50d69-138">NOTES</span></span>

## <span data-ttu-id="50d69-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50d69-139">RELATED LINKS</span></span>
