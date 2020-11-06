---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: f281192e22cd8acdf85e389d82ef7146590be158
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507479"
---
# <span data-ttu-id="52411-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="52411-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="52411-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52411-102">SYNOPSIS</span></span>
<span data-ttu-id="52411-103">Rimuove il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="52411-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52411-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52411-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52411-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52411-105">DESCRIPTION</span></span>
<span data-ttu-id="52411-106">Il cmdlet **Remove-AzureRmDataLakeStoreTrustedIdProvider** rimuove il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="52411-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="52411-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52411-107">EXAMPLES</span></span>

### <span data-ttu-id="52411-108">Esempio 1: rimuovere un provider di identità attendibile.</span><span class="sxs-lookup"><span data-stu-id="52411-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="52411-109">Rimuove il provider "fornitore" dall'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="52411-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="52411-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52411-110">PARAMETERS</span></span>

### <span data-ttu-id="52411-111">-Account</span><span class="sxs-lookup"><span data-stu-id="52411-111">-Account</span></span>
<span data-ttu-id="52411-112">L'account di data Lake Store per rimuovere il provider di identità attendibile da</span><span class="sxs-lookup"><span data-stu-id="52411-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="52411-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52411-113">-DefaultProfile</span></span>
<span data-ttu-id="52411-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="52411-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52411-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="52411-115">-Name</span></span>
<span data-ttu-id="52411-116">Nome del provider di identità attendibile.</span><span class="sxs-lookup"><span data-stu-id="52411-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="52411-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52411-117">-PassThru</span></span>
<span data-ttu-id="52411-118">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="52411-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="52411-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52411-119">-ResourceGroupName</span></span>
<span data-ttu-id="52411-120">Specifica il nome del gruppo di risorse che contiene l'account per cui rimuovere il provider di identità attendibile.</span><span class="sxs-lookup"><span data-stu-id="52411-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="52411-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52411-121">-Confirm</span></span>
<span data-ttu-id="52411-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52411-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52411-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52411-123">-WhatIf</span></span>
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

### <span data-ttu-id="52411-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52411-124">CommonParameters</span></span>
<span data-ttu-id="52411-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52411-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52411-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52411-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52411-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52411-127">INPUTS</span></span>

### <span data-ttu-id="52411-128">System. String</span><span class="sxs-lookup"><span data-stu-id="52411-128">System.String</span></span>

### <span data-ttu-id="52411-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="52411-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="52411-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52411-130">OUTPUTS</span></span>

### <span data-ttu-id="52411-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52411-131">System.Boolean</span></span>

## <span data-ttu-id="52411-132">Note</span><span class="sxs-lookup"><span data-stu-id="52411-132">NOTES</span></span>

## <span data-ttu-id="52411-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52411-133">RELATED LINKS</span></span>
