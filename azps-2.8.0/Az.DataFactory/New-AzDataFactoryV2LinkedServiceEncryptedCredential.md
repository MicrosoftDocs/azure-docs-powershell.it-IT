---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: bdc3d9b997a98ca67c2848ada32d8fc94fa20e09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674976"
---
# <span data-ttu-id="caadb-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="caadb-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="caadb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="caadb-102">SYNOPSIS</span></span>
<span data-ttu-id="caadb-103">Crittografare le credenziali nel servizio collegato con l'Integration runtime specificato.</span><span class="sxs-lookup"><span data-stu-id="caadb-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="caadb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="caadb-104">SYNTAX</span></span>

### <span data-ttu-id="caadb-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="caadb-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caadb-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="caadb-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caadb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="caadb-107">DESCRIPTION</span></span>
<span data-ttu-id="caadb-108">Il cmdlet New-AzDataFactoryV2LinkedServiceEncryptCredential crittografa le credenziali nel servizio collegato con l'Integration runtime specificato.</span><span class="sxs-lookup"><span data-stu-id="caadb-108">The New-AzDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="caadb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="caadb-109">EXAMPLES</span></span>

### <span data-ttu-id="caadb-110">Esempio 1: crittografare le credenziali in un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="caadb-110">Example 1: Encrypt credentials in a linked service</span></span>
```
PS C:\> New-AzDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="caadb-111">Questo comando crittografa le credenziali in file D:\sql.jscon il runtime di integrazione denominato myIR.</span><span class="sxs-lookup"><span data-stu-id="caadb-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="caadb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="caadb-112">PARAMETERS</span></span>

### <span data-ttu-id="caadb-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="caadb-113">-DataFactory</span></span>
<span data-ttu-id="caadb-114">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="caadb-114">The data factory object.</span></span>

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

### <span data-ttu-id="caadb-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="caadb-115">-DataFactoryName</span></span>
<span data-ttu-id="caadb-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="caadb-116">The data factory name.</span></span>

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

### <span data-ttu-id="caadb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caadb-117">-DefaultProfile</span></span>
<span data-ttu-id="caadb-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="caadb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caadb-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="caadb-119">-DefinitionFile</span></span>
<span data-ttu-id="caadb-120">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="caadb-120">The JSON file path.</span></span>

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

### <span data-ttu-id="caadb-121">-Force</span><span class="sxs-lookup"><span data-stu-id="caadb-121">-Force</span></span>
<span data-ttu-id="caadb-122">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="caadb-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="caadb-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="caadb-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="caadb-124">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="caadb-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="caadb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caadb-125">-ResourceGroupName</span></span>
<span data-ttu-id="caadb-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="caadb-126">The resource group name.</span></span>

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

### <span data-ttu-id="caadb-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="caadb-127">-Confirm</span></span>
<span data-ttu-id="caadb-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caadb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caadb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caadb-129">-WhatIf</span></span>
<span data-ttu-id="caadb-130">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="caadb-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="caadb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caadb-131">CommonParameters</span></span>
<span data-ttu-id="caadb-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caadb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caadb-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caadb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caadb-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="caadb-134">INPUTS</span></span>

### <span data-ttu-id="caadb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="caadb-135">System.String</span></span>

### <span data-ttu-id="caadb-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="caadb-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="caadb-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="caadb-137">OUTPUTS</span></span>

### <span data-ttu-id="caadb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="caadb-138">System.String</span></span>

## <span data-ttu-id="caadb-139">Note</span><span class="sxs-lookup"><span data-stu-id="caadb-139">NOTES</span></span>

## <span data-ttu-id="caadb-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="caadb-140">RELATED LINKS</span></span>
