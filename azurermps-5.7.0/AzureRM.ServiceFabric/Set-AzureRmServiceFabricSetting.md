---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 8296945de2bcf98213fc692e486e793a91f84939
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509607"
---
# <span data-ttu-id="7c8ad-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="7c8ad-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="7c8ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c8ad-102">SYNOPSIS</span></span>
<span data-ttu-id="7c8ad-103">Aggiungere o aggiornare una o più impostazioni del tessuto del servizio al cluster.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c8ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c8ad-104">SYNTAX</span></span>

### <span data-ttu-id="7c8ad-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="7c8ad-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c8ad-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="7c8ad-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c8ad-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c8ad-107">DESCRIPTION</span></span>
<span data-ttu-id="7c8ad-108">Usare **set-AzureRmServiceFabricSetting** per aggiungere o aggiornare le impostazioni del tessuto del servizio in un cluster.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="7c8ad-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c8ad-109">EXAMPLES</span></span>

### <span data-ttu-id="7c8ad-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c8ad-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="7c8ad-111">Questo comando imposterà "MaxFileOperationTimeout" sul valore "5000" nella sezione "NamingService".</span><span class="sxs-lookup"><span data-stu-id="7c8ad-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="7c8ad-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c8ad-112">PARAMETERS</span></span>

### <span data-ttu-id="7c8ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c8ad-113">-DefaultProfile</span></span>
<span data-ttu-id="7c8ad-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8ad-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c8ad-115">-Name</span></span>
<span data-ttu-id="7c8ad-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8ad-117">Parametro-</span><span class="sxs-lookup"><span data-stu-id="7c8ad-117">-Parameter</span></span>
<span data-ttu-id="7c8ad-118">Parametro.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-118">Parameter.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c8ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c8ad-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8ad-121">-Sezione</span><span class="sxs-lookup"><span data-stu-id="7c8ad-121">-Section</span></span>
<span data-ttu-id="7c8ad-122">Sezione.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-122">Section.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8ad-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="7c8ad-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="7c8ad-124">Tipo di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-124">Client authentication type.</span></span>

```yaml
Type: PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8ad-125">-Valore</span><span class="sxs-lookup"><span data-stu-id="7c8ad-125">-Value</span></span>
<span data-ttu-id="7c8ad-126">Valore.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-126">Value.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8ad-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c8ad-127">-Confirm</span></span>
<span data-ttu-id="7c8ad-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8ad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c8ad-129">-WhatIf</span></span>
<span data-ttu-id="7c8ad-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c8ad-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8ad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c8ad-132">CommonParameters</span></span>
<span data-ttu-id="7c8ad-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c8ad-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c8ad-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c8ad-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c8ad-135">INPUTS</span></span>

### <span data-ttu-id="7c8ad-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7c8ad-136">System.String</span></span>
<span data-ttu-id="7c8ad-137">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="7c8ad-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="7c8ad-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c8ad-138">OUTPUTS</span></span>

### <span data-ttu-id="7c8ad-139">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="7c8ad-139">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="7c8ad-140">Note</span><span class="sxs-lookup"><span data-stu-id="7c8ad-140">NOTES</span></span>

## <span data-ttu-id="7c8ad-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c8ad-141">RELATED LINKS</span></span>

