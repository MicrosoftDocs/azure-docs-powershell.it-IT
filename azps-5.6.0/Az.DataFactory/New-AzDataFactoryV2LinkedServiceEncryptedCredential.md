---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 678cc7e015321d90fee5a5340caeeeb861b30600
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971165"
---
# <span data-ttu-id="819d5-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="819d5-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="819d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="819d5-102">SYNOPSIS</span></span>
<span data-ttu-id="819d5-103">Crittografare le credenziali nel servizio collegato con il runtime di integrazione specificato.</span><span class="sxs-lookup"><span data-stu-id="819d5-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="819d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="819d5-104">SYNTAX</span></span>

### <span data-ttu-id="819d5-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="819d5-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="819d5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="819d5-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="819d5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="819d5-107">DESCRIPTION</span></span>
<span data-ttu-id="819d5-108">Il New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet crittografa le credenziali nel servizio collegato con il runtime di integrazione specificato.</span><span class="sxs-lookup"><span data-stu-id="819d5-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

<span data-ttu-id="819d5-109">Assicurarsi che siano soddisfatti i prerequisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="819d5-109">Please ensure the following prerequisites are met:</span></span>
* <span data-ttu-id="819d5-110">**L'opzione** di accesso remoto è abilitata nel runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="819d5-110">**Remote access** option is enabled on the self-hosted integration runtime.</span></span>
* <span data-ttu-id="819d5-111">Per eseguire il cmdlet si usa Powershell 7.0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="819d5-111">Powershell 7.0 or higher is used to execute the cmdlet.</span></span>

## <span data-ttu-id="819d5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="819d5-112">EXAMPLES</span></span>

### <span data-ttu-id="819d5-113">Esempio 1: Crittografare le credenziali in un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="819d5-113">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="819d5-114">Questo comando crittografa le credenziali nel file C:\samples\WikiSample\TaxiDemo1.jscon il runtime di integrazione denominato test-selfhost-ir.</span><span class="sxs-lookup"><span data-stu-id="819d5-114">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="819d5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="819d5-115">PARAMETERS</span></span>

### <span data-ttu-id="819d5-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="819d5-116">-DataFactory</span></span>
<span data-ttu-id="819d5-117">Oggetto data factory.</span><span class="sxs-lookup"><span data-stu-id="819d5-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="819d5-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="819d5-118">-DataFactoryName</span></span>
<span data-ttu-id="819d5-119">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="819d5-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="819d5-120">-DefaultProfile</span></span>
<span data-ttu-id="819d5-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="819d5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="819d5-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="819d5-122">-DefinitionFile</span></span>
<span data-ttu-id="819d5-123">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="819d5-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819d5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="819d5-124">-Force</span></span>
<span data-ttu-id="819d5-125">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="819d5-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="819d5-126">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="819d5-126">-IntegrationRuntimeName</span></span>
<span data-ttu-id="819d5-127">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="819d5-127">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819d5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="819d5-128">-ResourceGroupName</span></span>
<span data-ttu-id="819d5-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="819d5-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819d5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="819d5-130">-Confirm</span></span>
<span data-ttu-id="819d5-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="819d5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="819d5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="819d5-132">-WhatIf</span></span>
<span data-ttu-id="819d5-133">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="819d5-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="819d5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="819d5-134">CommonParameters</span></span>
<span data-ttu-id="819d5-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="819d5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="819d5-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="819d5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="819d5-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="819d5-137">INPUTS</span></span>

### <span data-ttu-id="819d5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="819d5-138">System.String</span></span>

### <span data-ttu-id="819d5-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="819d5-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="819d5-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="819d5-140">OUTPUTS</span></span>

### <span data-ttu-id="819d5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="819d5-141">System.String</span></span>

## <span data-ttu-id="819d5-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="819d5-142">NOTES</span></span>

## <span data-ttu-id="819d5-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="819d5-143">RELATED LINKS</span></span>
