---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 3e16db29f6560778dff5c86ac222d06fd41a5807
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209787"
---
# <span data-ttu-id="aab8c-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="aab8c-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="aab8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aab8c-102">SYNOPSIS</span></span>
<span data-ttu-id="aab8c-103">Rimuove il provider di identità attendibile specificato nel Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="aab8c-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="aab8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aab8c-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aab8c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aab8c-105">DESCRIPTION</span></span>
<span data-ttu-id="aab8c-106">Il cmdlet **Remove-AzDataLakeStoreTrustedIdProvider** rimuove il provider di identità attendibile specificato nel Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="aab8c-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="aab8c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aab8c-107">EXAMPLES</span></span>

### <span data-ttu-id="aab8c-108">Esempio 1: Rimuovere un provider di identità attendibile.</span><span class="sxs-lookup"><span data-stu-id="aab8c-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="aab8c-109">Rimuove il provider "MyProvider" dall'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="aab8c-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="aab8c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aab8c-110">PARAMETERS</span></span>

### <span data-ttu-id="aab8c-111">-Account</span><span class="sxs-lookup"><span data-stu-id="aab8c-111">-Account</span></span>
<span data-ttu-id="aab8c-112">Account Data Lake Store da cui rimuovere il provider di identità attendibile</span><span class="sxs-lookup"><span data-stu-id="aab8c-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="aab8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab8c-113">-DefaultProfile</span></span>
<span data-ttu-id="aab8c-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="aab8c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aab8c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="aab8c-115">-Name</span></span>
<span data-ttu-id="aab8c-116">Nome del provider di identità attendibile.</span><span class="sxs-lookup"><span data-stu-id="aab8c-116">The name of the trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aab8c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aab8c-117">-PassThru</span></span>
<span data-ttu-id="aab8c-118">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="aab8c-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="aab8c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aab8c-119">-ResourceGroupName</span></span>
<span data-ttu-id="aab8c-120">Specifica il nome del gruppo di risorse che contiene l'account da cui rimuovere il provider di identità attendibile.</span><span class="sxs-lookup"><span data-stu-id="aab8c-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aab8c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aab8c-121">-Confirm</span></span>
<span data-ttu-id="aab8c-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aab8c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aab8c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aab8c-123">-WhatIf</span></span>
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

### <span data-ttu-id="aab8c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab8c-124">CommonParameters</span></span>
<span data-ttu-id="aab8c-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aab8c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab8c-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aab8c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab8c-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="aab8c-127">INPUTS</span></span>

### <span data-ttu-id="aab8c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="aab8c-128">System.String</span></span>

### <span data-ttu-id="aab8c-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aab8c-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aab8c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aab8c-130">OUTPUTS</span></span>

### <span data-ttu-id="aab8c-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aab8c-131">System.Boolean</span></span>

## <span data-ttu-id="aab8c-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="aab8c-132">NOTES</span></span>

## <span data-ttu-id="aab8c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aab8c-133">RELATED LINKS</span></span>
