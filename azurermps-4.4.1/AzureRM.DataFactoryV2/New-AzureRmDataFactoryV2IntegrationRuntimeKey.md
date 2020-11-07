---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 166bae99bebbc5a1b1c25ffc79faa3a1f7254bbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685688"
---
# <span data-ttu-id="f00ad-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="f00ad-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="f00ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f00ad-102">SYNOPSIS</span></span>
<span data-ttu-id="f00ad-103">Rigenera automaticamente la chiave di runtime di integrazione ospitata.</span><span class="sxs-lookup"><span data-stu-id="f00ad-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f00ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f00ad-104">SYNTAX</span></span>

### <span data-ttu-id="f00ad-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f00ad-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f00ad-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f00ad-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="f00ad-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f00ad-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f00ad-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f00ad-108">DESCRIPTION</span></span>
<span data-ttu-id="f00ad-109">Il cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** rigenera la chiave di runtime Integration con il nome della chiave specificato dal parametro "Key Name".</span><span class="sxs-lookup"><span data-stu-id="f00ad-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="f00ad-110">La chiave precedente non è valida.</span><span class="sxs-lookup"><span data-stu-id="f00ad-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="f00ad-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f00ad-111">EXAMPLES</span></span>

### <span data-ttu-id="f00ad-112">Esempio 1: generare una nuova chiave per un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="f00ad-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="f00ad-113">Il cmdlet rigenera la chiave "authKey2" per Integration runtime denominata "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="f00ad-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="f00ad-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f00ad-114">PARAMETERS</span></span>

### <span data-ttu-id="f00ad-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f00ad-115">-Confirm</span></span>
<span data-ttu-id="f00ad-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f00ad-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f00ad-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f00ad-117">-DataFactoryName</span></span>
<span data-ttu-id="f00ad-118">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="f00ad-118">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00ad-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f00ad-119">-Force</span></span>
<span data-ttu-id="f00ad-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="f00ad-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00ad-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f00ad-121">-InputObject</span></span>
<span data-ttu-id="f00ad-122">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="f00ad-122">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f00ad-123">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="f00ad-123">-KeyName</span></span>
<span data-ttu-id="f00ad-124">Nome della chiave di autenticazione del runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="f00ad-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00ad-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f00ad-125">-Name</span></span>
<span data-ttu-id="f00ad-126">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f00ad-126">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00ad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f00ad-127">-ResourceGroupName</span></span>
<span data-ttu-id="f00ad-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f00ad-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00ad-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f00ad-129">-ResourceId</span></span>
<span data-ttu-id="f00ad-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="f00ad-130">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00ad-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f00ad-131">-WhatIf</span></span>
<span data-ttu-id="f00ad-132">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f00ad-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="f00ad-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f00ad-133">INPUTS</span></span>

### <span data-ttu-id="f00ad-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f00ad-134">System.String</span></span>
<span data-ttu-id="f00ad-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f00ad-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="f00ad-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f00ad-136">OUTPUTS</span></span>

### <span data-ttu-id="f00ad-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="f00ad-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="f00ad-138">Note</span><span class="sxs-lookup"><span data-stu-id="f00ad-138">NOTES</span></span>

## <span data-ttu-id="f00ad-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f00ad-139">RELATED LINKS</span></span>
[<span data-ttu-id="f00ad-140">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="f00ad-140">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
