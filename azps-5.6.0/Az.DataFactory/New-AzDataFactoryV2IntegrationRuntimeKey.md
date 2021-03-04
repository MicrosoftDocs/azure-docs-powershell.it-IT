---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 11d87742e34ae387f765551f93add5a1c300421a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971182"
---
# <span data-ttu-id="ef36c-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="ef36c-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="ef36c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef36c-102">SYNOPSIS</span></span>
<span data-ttu-id="ef36c-103">Rigenerare la chiave di runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="ef36c-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="ef36c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef36c-104">SYNTAX</span></span>

### <span data-ttu-id="ef36c-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ef36c-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef36c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef36c-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef36c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ef36c-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef36c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ef36c-108">DESCRIPTION</span></span>
<span data-ttu-id="ef36c-109">Il cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** rigenera la chiave di runtime di integrazione con il nome di chiave specificato dal parametro 'KeyName'.</span><span class="sxs-lookup"><span data-stu-id="ef36c-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="ef36c-110">La chiave precedente non è valida.</span><span class="sxs-lookup"><span data-stu-id="ef36c-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="ef36c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef36c-111">EXAMPLES</span></span>

### <span data-ttu-id="ef36c-112">Esempio 1: Generare una nuova chiave per un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="ef36c-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="ef36c-113">Il cmdlet rigenera la chiave "authKey2" per il runtime di integrazione denominato "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="ef36c-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="ef36c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef36c-114">PARAMETERS</span></span>

### <span data-ttu-id="ef36c-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ef36c-115">-DataFactoryName</span></span>
<span data-ttu-id="ef36c-116">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="ef36c-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef36c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef36c-117">-DefaultProfile</span></span>
<span data-ttu-id="ef36c-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef36c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef36c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ef36c-119">-Force</span></span>
<span data-ttu-id="ef36c-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ef36c-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ef36c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef36c-121">-InputObject</span></span>
<span data-ttu-id="ef36c-122">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ef36c-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef36c-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ef36c-123">-KeyName</span></span>
<span data-ttu-id="ef36c-124">Nome della chiave di autenticazione del runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="ef36c-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef36c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ef36c-125">-Name</span></span>
<span data-ttu-id="ef36c-126">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ef36c-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef36c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef36c-127">-ResourceGroupName</span></span>
<span data-ttu-id="ef36c-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ef36c-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef36c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef36c-129">-ResourceId</span></span>
<span data-ttu-id="ef36c-130">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="ef36c-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef36c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef36c-131">-Confirm</span></span>
<span data-ttu-id="ef36c-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef36c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef36c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef36c-133">-WhatIf</span></span>
<span data-ttu-id="ef36c-134">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="ef36c-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ef36c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef36c-135">CommonParameters</span></span>
<span data-ttu-id="ef36c-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef36c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef36c-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef36c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef36c-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="ef36c-138">INPUTS</span></span>

### <span data-ttu-id="ef36c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ef36c-139">System.String</span></span>

### <span data-ttu-id="ef36c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ef36c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ef36c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef36c-141">OUTPUTS</span></span>

### <span data-ttu-id="ef36c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="ef36c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="ef36c-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="ef36c-143">NOTES</span></span>

## <span data-ttu-id="ef36c-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef36c-144">RELATED LINKS</span></span>

[<span data-ttu-id="ef36c-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="ef36c-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
