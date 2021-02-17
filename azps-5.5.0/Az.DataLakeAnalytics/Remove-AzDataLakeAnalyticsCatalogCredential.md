---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 9fbc00fe190e0a53fc9c41a6894ec35a7f8d9129
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194807"
---
# <span data-ttu-id="a1590-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="a1590-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="a1590-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1590-102">SYNOPSIS</span></span>
<span data-ttu-id="a1590-103">Elimina le credenziali di Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a1590-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="a1590-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1590-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1590-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a1590-105">DESCRIPTION</span></span>
<span data-ttu-id="a1590-106">Il Remove-AzDataLakeAnalyticsCatalogCredential cmdlet elimina le credenziali del catalogo di Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a1590-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="a1590-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1590-107">EXAMPLES</span></span>

### <span data-ttu-id="a1590-108">Esempio 1: Rimuovere le credenziali</span><span class="sxs-lookup"><span data-stu-id="a1590-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="a1590-109">Questo comando rimuove le credenziali del catalogo di Data Lake Analytics specificate.</span><span class="sxs-lookup"><span data-stu-id="a1590-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="a1590-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1590-110">PARAMETERS</span></span>

### <span data-ttu-id="a1590-111">-Account</span><span class="sxs-lookup"><span data-stu-id="a1590-111">-Account</span></span>
<span data-ttu-id="a1590-112">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a1590-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a1590-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a1590-113">-DatabaseName</span></span>
<span data-ttu-id="a1590-114">Specifica il nome del database che contiene le credenziali.</span><span class="sxs-lookup"><span data-stu-id="a1590-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="a1590-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1590-115">-DefaultProfile</span></span>
<span data-ttu-id="a1590-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="a1590-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1590-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a1590-117">-Force</span></span>
<span data-ttu-id="a1590-118">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="a1590-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1590-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a1590-119">-Name</span></span>
<span data-ttu-id="a1590-120">Specifica il nome delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="a1590-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="a1590-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1590-121">-PassThru</span></span>
<span data-ttu-id="a1590-122">Indica che questo cmdlet non attende il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a1590-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="a1590-123">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a1590-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a1590-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a1590-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a1590-125">-Password</span><span class="sxs-lookup"><span data-stu-id="a1590-125">-Password</span></span>
<span data-ttu-id="a1590-126">La password per le credenziali.</span><span class="sxs-lookup"><span data-stu-id="a1590-126">The password for the credential.</span></span>
<span data-ttu-id="a1590-127">Questa operazione è necessaria se il chiamante non è il proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="a1590-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="a1590-128">-Ricorrenza</span><span class="sxs-lookup"><span data-stu-id="a1590-128">-Recurse</span></span>
<span data-ttu-id="a1590-129">Indica che l'operazione di eliminazione deve essere completata ed eliminare anche tutte le risorse che dipendono da questa credenziali.</span><span class="sxs-lookup"><span data-stu-id="a1590-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="a1590-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1590-130">-Confirm</span></span>
<span data-ttu-id="a1590-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1590-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1590-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1590-132">-WhatIf</span></span>
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

### <span data-ttu-id="a1590-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1590-133">CommonParameters</span></span>
<span data-ttu-id="a1590-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1590-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1590-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1590-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1590-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="a1590-136">INPUTS</span></span>

### <span data-ttu-id="a1590-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a1590-137">System.String</span></span>

### <span data-ttu-id="a1590-138">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="a1590-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="a1590-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a1590-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a1590-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1590-140">OUTPUTS</span></span>

### <span data-ttu-id="a1590-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a1590-141">System.Boolean</span></span>

## <span data-ttu-id="a1590-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="a1590-142">NOTES</span></span>

## <span data-ttu-id="a1590-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1590-143">RELATED LINKS</span></span>
