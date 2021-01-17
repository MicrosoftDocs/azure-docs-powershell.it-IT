---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 07cb597f5ca3793e3eb8db3fe153fafaa94f3501
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324489"
---
# <span data-ttu-id="662e8-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="662e8-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="662e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="662e8-102">SYNOPSIS</span></span>
<span data-ttu-id="662e8-103">Rigenera automaticamente la chiave di runtime di integrazione ospitata.</span><span class="sxs-lookup"><span data-stu-id="662e8-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="662e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="662e8-104">SYNTAX</span></span>

### <span data-ttu-id="662e8-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="662e8-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="662e8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="662e8-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="662e8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="662e8-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="662e8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="662e8-108">DESCRIPTION</span></span>
<span data-ttu-id="662e8-109">Il cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** rigenera la chiave di runtime Integration con il nome della chiave specificato dal parametro "Key Name".</span><span class="sxs-lookup"><span data-stu-id="662e8-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="662e8-110">La chiave precedente non è valida.</span><span class="sxs-lookup"><span data-stu-id="662e8-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="662e8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="662e8-111">EXAMPLES</span></span>

### <span data-ttu-id="662e8-112">Esempio 1: generare una nuova chiave per un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="662e8-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="662e8-113">Il cmdlet rigenera la chiave "authKey2" per Integration runtime denominata "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="662e8-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="662e8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="662e8-114">PARAMETERS</span></span>

### <span data-ttu-id="662e8-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="662e8-115">-DataFactoryName</span></span>
<span data-ttu-id="662e8-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="662e8-116">The data factory name.</span></span>

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

### <span data-ttu-id="662e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="662e8-117">-DefaultProfile</span></span>
<span data-ttu-id="662e8-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="662e8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="662e8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="662e8-119">-Force</span></span>
<span data-ttu-id="662e8-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="662e8-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="662e8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="662e8-121">-InputObject</span></span>
<span data-ttu-id="662e8-122">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="662e8-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="662e8-123">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="662e8-123">-KeyName</span></span>
<span data-ttu-id="662e8-124">Nome della chiave di autenticazione del runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="662e8-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="662e8-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="662e8-125">-Name</span></span>
<span data-ttu-id="662e8-126">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="662e8-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="662e8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="662e8-127">-ResourceGroupName</span></span>
<span data-ttu-id="662e8-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="662e8-128">The resource group name.</span></span>

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

### <span data-ttu-id="662e8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="662e8-129">-ResourceId</span></span>
<span data-ttu-id="662e8-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="662e8-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="662e8-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="662e8-131">-Confirm</span></span>
<span data-ttu-id="662e8-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="662e8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="662e8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="662e8-133">-WhatIf</span></span>
<span data-ttu-id="662e8-134">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="662e8-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="662e8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="662e8-135">CommonParameters</span></span>
<span data-ttu-id="662e8-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="662e8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="662e8-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="662e8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="662e8-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="662e8-138">INPUTS</span></span>

### <span data-ttu-id="662e8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="662e8-139">System.String</span></span>

### <span data-ttu-id="662e8-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="662e8-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="662e8-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="662e8-141">OUTPUTS</span></span>

### <span data-ttu-id="662e8-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="662e8-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="662e8-143">Note</span><span class="sxs-lookup"><span data-stu-id="662e8-143">NOTES</span></span>

## <span data-ttu-id="662e8-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="662e8-144">RELATED LINKS</span></span>

[<span data-ttu-id="662e8-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="662e8-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
