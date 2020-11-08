---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: db6d94b4aa2f6182abc114f11d1dba0b40ebbb93
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193813"
---
# <span data-ttu-id="be120-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="be120-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="be120-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be120-102">SYNOPSIS</span></span>
<span data-ttu-id="be120-103">Rimuovere una o più impostazioni del tessuto del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="be120-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="be120-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be120-104">SYNTAX</span></span>

### <span data-ttu-id="be120-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="be120-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be120-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="be120-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be120-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be120-107">DESCRIPTION</span></span>
<span data-ttu-id="be120-108">Usare **Remove-AzServiceFabricSetting** per rimuovere le impostazioni del tessuto del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="be120-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="be120-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be120-109">EXAMPLES</span></span>

### <span data-ttu-id="be120-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="be120-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="be120-111">Questo comando rimuove le impostazioni "MaxCursors" nella sezione "EseStore".</span><span class="sxs-lookup"><span data-stu-id="be120-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="be120-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be120-112">PARAMETERS</span></span>

### <span data-ttu-id="be120-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be120-113">-DefaultProfile</span></span>
<span data-ttu-id="be120-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be120-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be120-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="be120-115">-Name</span></span>
<span data-ttu-id="be120-116">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="be120-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="be120-117">Parametro-</span><span class="sxs-lookup"><span data-stu-id="be120-117">-Parameter</span></span>
<span data-ttu-id="be120-118">Nome parametro dell'impostazione del tessuto</span><span class="sxs-lookup"><span data-stu-id="be120-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="be120-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be120-119">-ResourceGroupName</span></span>
<span data-ttu-id="be120-120">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="be120-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="be120-121">-Sezione</span><span class="sxs-lookup"><span data-stu-id="be120-121">-Section</span></span>
<span data-ttu-id="be120-122">Nome sezione dell'impostazione del tessuto</span><span class="sxs-lookup"><span data-stu-id="be120-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="be120-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="be120-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="be120-124">Matrice di impostazioni del tessuto</span><span class="sxs-lookup"><span data-stu-id="be120-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="be120-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="be120-125">-Confirm</span></span>
<span data-ttu-id="be120-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be120-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be120-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be120-127">-WhatIf</span></span>
<span data-ttu-id="be120-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be120-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be120-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be120-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be120-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be120-130">CommonParameters</span></span>
<span data-ttu-id="be120-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be120-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be120-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be120-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be120-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be120-133">INPUTS</span></span>

### <span data-ttu-id="be120-134">System. String</span><span class="sxs-lookup"><span data-stu-id="be120-134">System.String</span></span>

### <span data-ttu-id="be120-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="be120-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="be120-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be120-136">OUTPUTS</span></span>

### <span data-ttu-id="be120-137">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="be120-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="be120-138">Note</span><span class="sxs-lookup"><span data-stu-id="be120-138">NOTES</span></span>

## <span data-ttu-id="be120-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be120-139">RELATED LINKS</span></span>