---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 79e5823c797c878643ea6ad2870873da363d0312
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674862"
---
# <span data-ttu-id="aacc3-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="aacc3-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="aacc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aacc3-102">SYNOPSIS</span></span>
<span data-ttu-id="aacc3-103">Elimina una credenziale di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="aacc3-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="aacc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aacc3-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aacc3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aacc3-105">DESCRIPTION</span></span>
<span data-ttu-id="aacc3-106">Il cmdlet Remove-AzDataLakeAnalyticsCatalogCredential Elimina le credenziali di un catalogo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="aacc3-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="aacc3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aacc3-107">EXAMPLES</span></span>

### <span data-ttu-id="aacc3-108">Esempio 1: rimuovere una credenziale</span><span class="sxs-lookup"><span data-stu-id="aacc3-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="aacc3-109">Questo comando consente di rimuovere le credenziali del catalogo dei dati del lago analitico specificato.</span><span class="sxs-lookup"><span data-stu-id="aacc3-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="aacc3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aacc3-110">PARAMETERS</span></span>

### <span data-ttu-id="aacc3-111">-Account</span><span class="sxs-lookup"><span data-stu-id="aacc3-111">-Account</span></span>
<span data-ttu-id="aacc3-112">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="aacc3-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="aacc3-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aacc3-113">-DatabaseName</span></span>
<span data-ttu-id="aacc3-114">Specifica il nome del database che contiene le credenziali.</span><span class="sxs-lookup"><span data-stu-id="aacc3-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="aacc3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aacc3-115">-DefaultProfile</span></span>
<span data-ttu-id="aacc3-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="aacc3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aacc3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="aacc3-117">-Force</span></span>
<span data-ttu-id="aacc3-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="aacc3-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aacc3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="aacc3-119">-Name</span></span>
<span data-ttu-id="aacc3-120">Specifica il nome della credenziale.</span><span class="sxs-lookup"><span data-stu-id="aacc3-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="aacc3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aacc3-121">-PassThru</span></span>
<span data-ttu-id="aacc3-122">Indica che il cmdlet non attende il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="aacc3-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="aacc3-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="aacc3-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aacc3-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="aacc3-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aacc3-125">-Password</span><span class="sxs-lookup"><span data-stu-id="aacc3-125">-Password</span></span>
<span data-ttu-id="aacc3-126">La password per la credenziale.</span><span class="sxs-lookup"><span data-stu-id="aacc3-126">The password for the credential.</span></span>
<span data-ttu-id="aacc3-127">Questa operazione è obbligatoria se il chiamante non è il proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="aacc3-127">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacc3-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="aacc3-128">-Recurse</span></span>
<span data-ttu-id="aacc3-129">Indica che questa operazione di eliminazione deve passare e anche eliminare e rilasciare tutte le risorse dipendenti da questa credenziale.</span><span class="sxs-lookup"><span data-stu-id="aacc3-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacc3-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aacc3-130">-Confirm</span></span>
<span data-ttu-id="aacc3-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aacc3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aacc3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aacc3-132">-WhatIf</span></span>
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

### <span data-ttu-id="aacc3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aacc3-133">CommonParameters</span></span>
<span data-ttu-id="aacc3-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aacc3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aacc3-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aacc3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aacc3-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aacc3-136">INPUTS</span></span>

### <span data-ttu-id="aacc3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="aacc3-137">System.String</span></span>

### <span data-ttu-id="aacc3-138">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="aacc3-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="aacc3-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aacc3-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aacc3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aacc3-140">OUTPUTS</span></span>

### <span data-ttu-id="aacc3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aacc3-141">System.Boolean</span></span>

## <span data-ttu-id="aacc3-142">Note</span><span class="sxs-lookup"><span data-stu-id="aacc3-142">NOTES</span></span>

## <span data-ttu-id="aacc3-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aacc3-143">RELATED LINKS</span></span>
