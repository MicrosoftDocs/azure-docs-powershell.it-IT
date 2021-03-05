---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: f14448e7b7606f37f5ffdee8c944d48a557c1f0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998380"
---
# <span data-ttu-id="2eb8c-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="2eb8c-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="2eb8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eb8c-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb8c-103">Elimina le credenziali di Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="2eb8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2eb8c-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eb8c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2eb8c-105">DESCRIPTION</span></span>
<span data-ttu-id="2eb8c-106">Il Remove-AzDataLakeAnalyticsCatalogCredential cmdlet elimina le credenziali del catalogo di Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="2eb8c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2eb8c-107">EXAMPLES</span></span>

### <span data-ttu-id="2eb8c-108">Esempio 1: Rimuovere le credenziali</span><span class="sxs-lookup"><span data-stu-id="2eb8c-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="2eb8c-109">Questo comando rimuove le credenziali del catalogo di Data Lake Analytics specificate.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="2eb8c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eb8c-110">PARAMETERS</span></span>

### <span data-ttu-id="2eb8c-111">-Account</span><span class="sxs-lookup"><span data-stu-id="2eb8c-111">-Account</span></span>
<span data-ttu-id="2eb8c-112">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="2eb8c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2eb8c-113">-DatabaseName</span></span>
<span data-ttu-id="2eb8c-114">Specifica il nome del database che contiene le credenziali.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="2eb8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb8c-115">-DefaultProfile</span></span>
<span data-ttu-id="2eb8c-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2eb8c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2eb8c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2eb8c-117">-Force</span></span>
<span data-ttu-id="2eb8c-118">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2eb8c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2eb8c-119">-Name</span></span>
<span data-ttu-id="2eb8c-120">Specifica il nome delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="2eb8c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2eb8c-121">-PassThru</span></span>
<span data-ttu-id="2eb8c-122">Indica che questo cmdlet non attende il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="2eb8c-123">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2eb8c-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2eb8c-125">-Password</span><span class="sxs-lookup"><span data-stu-id="2eb8c-125">-Password</span></span>
<span data-ttu-id="2eb8c-126">La password per le credenziali.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-126">The password for the credential.</span></span>
<span data-ttu-id="2eb8c-127">Questa operazione è necessaria se il chiamante non è il proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="2eb8c-128">-Ricorrenza</span><span class="sxs-lookup"><span data-stu-id="2eb8c-128">-Recurse</span></span>
<span data-ttu-id="2eb8c-129">Indica che l'operazione di eliminazione deve essere completata ed eliminare anche tutte le risorse che dipendono da queste credenziali.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="2eb8c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2eb8c-130">-Confirm</span></span>
<span data-ttu-id="2eb8c-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eb8c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb8c-132">-WhatIf</span></span>
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

### <span data-ttu-id="2eb8c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb8c-133">CommonParameters</span></span>
<span data-ttu-id="2eb8c-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb8c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb8c-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eb8c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb8c-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="2eb8c-136">INPUTS</span></span>

### <span data-ttu-id="2eb8c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2eb8c-137">System.String</span></span>

### <span data-ttu-id="2eb8c-138">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="2eb8c-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="2eb8c-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2eb8c-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2eb8c-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2eb8c-140">OUTPUTS</span></span>

### <span data-ttu-id="2eb8c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2eb8c-141">System.Boolean</span></span>

## <span data-ttu-id="2eb8c-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="2eb8c-142">NOTES</span></span>

## <span data-ttu-id="2eb8c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2eb8c-143">RELATED LINKS</span></span>
