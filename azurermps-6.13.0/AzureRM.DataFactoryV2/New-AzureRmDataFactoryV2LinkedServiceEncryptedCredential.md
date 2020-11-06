---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 765bd2c75a377204ab4566f47d0498deaf127953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507535"
---
# <span data-ttu-id="d869e-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="d869e-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="d869e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d869e-102">SYNOPSIS</span></span>
<span data-ttu-id="d869e-103">Crittografare le credenziali nel servizio collegato con l'Integration runtime specificato.</span><span class="sxs-lookup"><span data-stu-id="d869e-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d869e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d869e-104">SYNTAX</span></span>

### <span data-ttu-id="d869e-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d869e-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d869e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d869e-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d869e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d869e-107">DESCRIPTION</span></span>
<span data-ttu-id="d869e-108">Il cmdlet New-AzureRmDataFactoryV2LinkedServiceEncryptCredential crittografa le credenziali nel servizio collegato con l'Integration runtime specificato.</span><span class="sxs-lookup"><span data-stu-id="d869e-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="d869e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d869e-109">EXAMPLES</span></span>

### <span data-ttu-id="d869e-110">Esempio 1: crittografare creadentials in un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="d869e-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="d869e-111">Questo comando crittografa le credenziali in file D:\sql.jscon il runtime di integrazione denominato myIR.</span><span class="sxs-lookup"><span data-stu-id="d869e-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="d869e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d869e-112">PARAMETERS</span></span>

### <span data-ttu-id="d869e-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d869e-113">-DataFactory</span></span>
<span data-ttu-id="d869e-114">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d869e-114">The data factory object.</span></span>

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

### <span data-ttu-id="d869e-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d869e-115">-DataFactoryName</span></span>
<span data-ttu-id="d869e-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="d869e-116">The data factory name.</span></span>

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

### <span data-ttu-id="d869e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d869e-117">-DefaultProfile</span></span>
<span data-ttu-id="d869e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d869e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d869e-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="d869e-119">-DefinitionFile</span></span>
<span data-ttu-id="d869e-120">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="d869e-120">The JSON file path.</span></span>

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

### <span data-ttu-id="d869e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d869e-121">-Force</span></span>
<span data-ttu-id="d869e-122">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d869e-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d869e-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="d869e-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="d869e-124">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d869e-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="d869e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d869e-125">-ResourceGroupName</span></span>
<span data-ttu-id="d869e-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d869e-126">The resource group name.</span></span>

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

### <span data-ttu-id="d869e-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d869e-127">-Confirm</span></span>
<span data-ttu-id="d869e-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d869e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d869e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d869e-129">-WhatIf</span></span>
<span data-ttu-id="d869e-130">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d869e-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d869e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d869e-131">CommonParameters</span></span>
<span data-ttu-id="d869e-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d869e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d869e-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d869e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d869e-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d869e-134">INPUTS</span></span>

### <span data-ttu-id="d869e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d869e-135">System.String</span></span>

### <span data-ttu-id="d869e-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d869e-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="d869e-137">Parametri: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d869e-137">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="d869e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d869e-138">OUTPUTS</span></span>

### <span data-ttu-id="d869e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d869e-139">System.String</span></span>

## <span data-ttu-id="d869e-140">Note</span><span class="sxs-lookup"><span data-stu-id="d869e-140">NOTES</span></span>

## <span data-ttu-id="d869e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d869e-141">RELATED LINKS</span></span>
