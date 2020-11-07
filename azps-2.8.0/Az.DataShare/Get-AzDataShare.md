---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a7780b18ba46b4a9e007eb4bb8ad84490bd73577
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674703"
---
# <span data-ttu-id="1c278-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="1c278-101">Get-AzDataShare</span></span>

## <span data-ttu-id="1c278-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c278-102">SYNOPSIS</span></span>
<span data-ttu-id="1c278-103">Ottenere informazioni sulle condivisioni dati.</span><span class="sxs-lookup"><span data-stu-id="1c278-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="1c278-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c278-104">SYNTAX</span></span>

### <span data-ttu-id="1c278-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c278-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c278-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c278-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c278-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c278-107">DESCRIPTION</span></span>
<span data-ttu-id="1c278-108">Il cmdlet **Get-AzDataShare** ottiene informazioni sulle condivisioni di dati in una condivisione dati di Azure accoount.</span><span class="sxs-lookup"><span data-stu-id="1c278-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="1c278-109">Se specifichi il nome di una condivisione dati, questo cmdlet ottiene le informazioni sulla condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="1c278-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="1c278-110">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutte le condivisioni di dati in un account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="1c278-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="1c278-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c278-111">EXAMPLES</span></span>

### <span data-ttu-id="1c278-112">Esempio 1: ottenere una condivisione dati specifica</span><span class="sxs-lookup"><span data-stu-id="1c278-112">Example 1 : Get a specific data share</span></span>
```
PS C:\>Get-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="1c278-113">Questo comando Visualizza le informazioni sulla condivisione di dati AdsShare nell'account di condivisione dati di Azure WikiAdsAccount e gli annunci del gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="1c278-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="1c278-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c278-114">PARAMETERS</span></span>

### <span data-ttu-id="1c278-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1c278-115">-AccountName</span></span>
<span data-ttu-id="1c278-116">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="1c278-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c278-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c278-117">-DefaultProfile</span></span>
<span data-ttu-id="1c278-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c278-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c278-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c278-119">-Name</span></span>
<span data-ttu-id="1c278-120">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="1c278-120">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c278-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c278-121">-ResourceGroupName</span></span>
<span data-ttu-id="1c278-122">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="1c278-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c278-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c278-123">-ResourceId</span></span>
<span data-ttu-id="1c278-124">ID risorsa della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="1c278-124">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c278-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c278-125">CommonParameters</span></span>
<span data-ttu-id="1c278-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c278-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c278-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c278-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c278-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c278-128">INPUTS</span></span>

### <span data-ttu-id="1c278-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1c278-129">System.String</span></span>

## <span data-ttu-id="1c278-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c278-130">OUTPUTS</span></span>

### <span data-ttu-id="1c278-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="1c278-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="1c278-132">Note</span><span class="sxs-lookup"><span data-stu-id="1c278-132">NOTES</span></span>

## <span data-ttu-id="1c278-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c278-133">RELATED LINKS</span></span>