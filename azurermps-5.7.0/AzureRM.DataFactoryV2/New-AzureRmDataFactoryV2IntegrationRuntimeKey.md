---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 2ac4868905ee1de93f87ecb17d6b9ced0f036cda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508224"
---
# <span data-ttu-id="50017-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="50017-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="50017-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50017-102">SYNOPSIS</span></span>
<span data-ttu-id="50017-103">Rigenera automaticamente la chiave di runtime di integrazione ospitata.</span><span class="sxs-lookup"><span data-stu-id="50017-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50017-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50017-104">SYNTAX</span></span>

### <span data-ttu-id="50017-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50017-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50017-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="50017-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50017-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="50017-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50017-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50017-108">DESCRIPTION</span></span>
<span data-ttu-id="50017-109">Il cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** rigenera la chiave di runtime Integration con il nome della chiave specificato dal parametro "Key Name".</span><span class="sxs-lookup"><span data-stu-id="50017-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="50017-110">La chiave precedente non è valida.</span><span class="sxs-lookup"><span data-stu-id="50017-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="50017-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50017-111">EXAMPLES</span></span>

### <span data-ttu-id="50017-112">Esempio 1: generare una nuova chiave per un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="50017-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="50017-113">Il cmdlet rigenera la chiave "authKey2" per Integration runtime denominata "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="50017-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="50017-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50017-114">PARAMETERS</span></span>

### <span data-ttu-id="50017-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="50017-115">-DataFactoryName</span></span>
<span data-ttu-id="50017-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="50017-116">The data factory name.</span></span>

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

### <span data-ttu-id="50017-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50017-117">-DefaultProfile</span></span>
<span data-ttu-id="50017-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50017-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50017-119">-Force</span><span class="sxs-lookup"><span data-stu-id="50017-119">-Force</span></span>
<span data-ttu-id="50017-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="50017-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="50017-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50017-121">-InputObject</span></span>
<span data-ttu-id="50017-122">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="50017-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="50017-123">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="50017-123">-KeyName</span></span>
<span data-ttu-id="50017-124">Nome della chiave di autenticazione del runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="50017-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="50017-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="50017-125">-Name</span></span>
<span data-ttu-id="50017-126">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="50017-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="50017-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50017-127">-ResourceGroupName</span></span>
<span data-ttu-id="50017-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50017-128">The resource group name.</span></span>

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

### <span data-ttu-id="50017-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50017-129">-ResourceId</span></span>
<span data-ttu-id="50017-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="50017-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="50017-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50017-131">-Confirm</span></span>
<span data-ttu-id="50017-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50017-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50017-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50017-133">-WhatIf</span></span>
<span data-ttu-id="50017-134">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50017-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="50017-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50017-135">CommonParameters</span></span>
<span data-ttu-id="50017-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50017-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50017-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50017-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50017-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50017-138">INPUTS</span></span>

### <span data-ttu-id="50017-139">System. String</span><span class="sxs-lookup"><span data-stu-id="50017-139">System.String</span></span>
<span data-ttu-id="50017-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="50017-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="50017-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50017-141">OUTPUTS</span></span>

### <span data-ttu-id="50017-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="50017-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="50017-143">Note</span><span class="sxs-lookup"><span data-stu-id="50017-143">NOTES</span></span>

## <span data-ttu-id="50017-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50017-144">RELATED LINKS</span></span>

[<span data-ttu-id="50017-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="50017-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
