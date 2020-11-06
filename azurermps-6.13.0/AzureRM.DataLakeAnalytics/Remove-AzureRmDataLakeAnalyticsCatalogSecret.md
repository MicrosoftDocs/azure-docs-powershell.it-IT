---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: aa7dace3141210e8c4ff6055a011f34523c5b586
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511755"
---
# <span data-ttu-id="5ce7c-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="5ce7c-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="5ce7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ce7c-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce7c-103">Elimina un segreto di analisi dei dati di Lake.</span><span class="sxs-lookup"><span data-stu-id="5ce7c-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ce7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ce7c-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ce7c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ce7c-105">DESCRIPTION</span></span>
<span data-ttu-id="5ce7c-106">Il cmdlet **Remove-AzureRmDataLakeAnalyticsCatalogSecret** Elimina un segreto del catalogo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce7c-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="5ce7c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ce7c-107">EXAMPLES</span></span>

### <span data-ttu-id="5ce7c-108">Esempio 1: rimuovere un segreto</span><span class="sxs-lookup"><span data-stu-id="5ce7c-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="5ce7c-109">Questo comando rimuove il segreto del catalogo dei dati di analisi del lago specificato.</span><span class="sxs-lookup"><span data-stu-id="5ce7c-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="5ce7c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ce7c-110">PARAMETERS</span></span>

### <span data-ttu-id="5ce7c-111">-Account</span><span class="sxs-lookup"><span data-stu-id="5ce7c-111">-Account</span></span>
<span data-ttu-id="5ce7c-112">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="5ce7c-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce7c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ce7c-113">-DatabaseName</span></span>
<span data-ttu-id="5ce7c-114">Specifica il nome del database che contiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="5ce7c-114">Specifies the name of the database that holds the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce7c-115">-DefaultProfile</span></span>
<span data-ttu-id="5ce7c-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5ce7c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ce7c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5ce7c-117">-Force</span></span>
<span data-ttu-id="5ce7c-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5ce7c-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce7c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ce7c-119">-Name</span></span>
<span data-ttu-id="5ce7c-120">Specifica il nome del segreto.</span><span class="sxs-lookup"><span data-stu-id="5ce7c-120">Specifies the name of the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce7c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ce7c-121">-PassThru</span></span>
<span data-ttu-id="5ce7c-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="5ce7c-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5ce7c-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="5ce7c-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce7c-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5ce7c-124">-Confirm</span></span>
<span data-ttu-id="5ce7c-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ce7c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce7c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce7c-126">-WhatIf</span></span>
<span data-ttu-id="5ce7c-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ce7c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ce7c-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ce7c-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce7c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce7c-129">CommonParameters</span></span>
<span data-ttu-id="5ce7c-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce7c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce7c-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ce7c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce7c-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ce7c-132">INPUTS</span></span>

### <span data-ttu-id="5ce7c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5ce7c-133">System.String</span></span>

## <span data-ttu-id="5ce7c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ce7c-134">OUTPUTS</span></span>

### <span data-ttu-id="5ce7c-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ce7c-135">System.Boolean</span></span>

## <span data-ttu-id="5ce7c-136">Note</span><span class="sxs-lookup"><span data-stu-id="5ce7c-136">NOTES</span></span>

## <span data-ttu-id="5ce7c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ce7c-137">RELATED LINKS</span></span>

[<span data-ttu-id="5ce7c-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="5ce7c-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="5ce7c-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="5ce7c-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


