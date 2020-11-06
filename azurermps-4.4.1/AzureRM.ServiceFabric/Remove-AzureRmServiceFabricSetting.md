---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 6fe4d0c3a32cd96693d64e46f9d8596083dd9c5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512932"
---
# <span data-ttu-id="103c7-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="103c7-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="103c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="103c7-102">SYNOPSIS</span></span>
<span data-ttu-id="103c7-103">Rimuovere una o più impostazioni del tessuto del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="103c7-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="103c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="103c7-104">SYNTAX</span></span>

### <span data-ttu-id="103c7-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="103c7-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="103c7-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="103c7-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="103c7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="103c7-107">DESCRIPTION</span></span>
<span data-ttu-id="103c7-108">Usare **Remove-AzureRmServiceFabricSetting** per rimuovere le impostazioni del tessuto del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="103c7-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="103c7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="103c7-109">EXAMPLES</span></span>

### <span data-ttu-id="103c7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="103c7-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="103c7-111">Questo comando rimuove le impostazioni "MaxCursors" nella sezione "EseStore".</span><span class="sxs-lookup"><span data-stu-id="103c7-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="103c7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="103c7-112">PARAMETERS</span></span>

### <span data-ttu-id="103c7-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="103c7-113">-Name</span></span>
<span data-ttu-id="103c7-114">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="103c7-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="103c7-115">Parametro-</span><span class="sxs-lookup"><span data-stu-id="103c7-115">-Parameter</span></span>
<span data-ttu-id="103c7-116">Parametro.</span><span class="sxs-lookup"><span data-stu-id="103c7-116">Parameter.</span></span>

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

### <span data-ttu-id="103c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="103c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="103c7-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="103c7-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="103c7-119">-Sezione</span><span class="sxs-lookup"><span data-stu-id="103c7-119">-Section</span></span>
<span data-ttu-id="103c7-120">Sezione.</span><span class="sxs-lookup"><span data-stu-id="103c7-120">Section.</span></span>

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

### <span data-ttu-id="103c7-121">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="103c7-121">-SettingsSectionDescription</span></span>
<span data-ttu-id="103c7-122">Tipo di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="103c7-122">Client authentication type.</span></span>

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

### <span data-ttu-id="103c7-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="103c7-123">-Confirm</span></span>
<span data-ttu-id="103c7-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="103c7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="103c7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="103c7-125">-WhatIf</span></span>
<span data-ttu-id="103c7-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="103c7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="103c7-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="103c7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="103c7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="103c7-128">-DefaultProfile</span></span>
<span data-ttu-id="103c7-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="103c7-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="103c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="103c7-130">CommonParameters</span></span>
<span data-ttu-id="103c7-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="103c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="103c7-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="103c7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="103c7-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="103c7-133">INPUTS</span></span>

### <span data-ttu-id="103c7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="103c7-134">System.String</span></span>
<span data-ttu-id="103c7-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="103c7-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="103c7-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="103c7-136">OUTPUTS</span></span>

### <span data-ttu-id="103c7-137">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="103c7-137">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="103c7-138">Note</span><span class="sxs-lookup"><span data-stu-id="103c7-138">NOTES</span></span>

## <span data-ttu-id="103c7-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="103c7-139">RELATED LINKS</span></span>

