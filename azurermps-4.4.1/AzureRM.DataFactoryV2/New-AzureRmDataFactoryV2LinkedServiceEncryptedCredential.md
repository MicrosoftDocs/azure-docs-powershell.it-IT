---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 9960a34d19c4016461ddfc53a37f83d3e73e7526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687534"
---
# <span data-ttu-id="6300f-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="6300f-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="6300f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6300f-102">SYNOPSIS</span></span>
<span data-ttu-id="6300f-103">Crittografare le credenziali nel servizio collegato con l'Integration runtime specificato.</span><span class="sxs-lookup"><span data-stu-id="6300f-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6300f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6300f-104">SYNTAX</span></span>

### <span data-ttu-id="6300f-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6300f-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6300f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6300f-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6300f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6300f-107">DESCRIPTION</span></span>
<span data-ttu-id="6300f-108">Il cmdlet New-AzureRmDataFactoryV2LinkedServiceEncryptCredential crittografa le credenziali nel servizio collegato con l'Integration runtime specificato.</span><span class="sxs-lookup"><span data-stu-id="6300f-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="6300f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6300f-109">EXAMPLES</span></span>

### <span data-ttu-id="6300f-110">Esempio 1: crittografare creadentials in un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="6300f-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="6300f-111">Questo comando crittografa le credenziali in file D:\sql.jscon il runtime di integrazione denominato myIR.</span><span class="sxs-lookup"><span data-stu-id="6300f-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="6300f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6300f-112">PARAMETERS</span></span>

### <span data-ttu-id="6300f-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6300f-113">-DataFactory</span></span>
<span data-ttu-id="6300f-114">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="6300f-114">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6300f-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6300f-115">-DataFactoryName</span></span>
<span data-ttu-id="6300f-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="6300f-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6300f-117">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="6300f-117">-DefinitionFile</span></span>
<span data-ttu-id="6300f-118">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="6300f-118">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6300f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6300f-119">-Force</span></span>
<span data-ttu-id="6300f-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6300f-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6300f-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6300f-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="6300f-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6300f-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6300f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6300f-123">-ResourceGroupName</span></span>
<span data-ttu-id="6300f-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6300f-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6300f-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6300f-125">-Confirm</span></span>
<span data-ttu-id="6300f-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6300f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6300f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6300f-127">-WhatIf</span></span>
<span data-ttu-id="6300f-128">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6300f-128">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="6300f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6300f-129">INPUTS</span></span>

### <span data-ttu-id="6300f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6300f-130">System.String</span></span>
<span data-ttu-id="6300f-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6300f-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="6300f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6300f-132">OUTPUTS</span></span>

### <span data-ttu-id="6300f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6300f-133">System.String</span></span>


## <span data-ttu-id="6300f-134">Note</span><span class="sxs-lookup"><span data-stu-id="6300f-134">NOTES</span></span>

## <span data-ttu-id="6300f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6300f-135">RELATED LINKS</span></span>

