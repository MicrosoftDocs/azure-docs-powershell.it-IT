---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195095"
---
# <span data-ttu-id="11694-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="11694-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="11694-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11694-102">SYNOPSIS</span></span>
<span data-ttu-id="11694-103">Ottiene le chiavi API per un account.</span><span class="sxs-lookup"><span data-stu-id="11694-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="11694-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11694-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11694-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="11694-105">DESCRIPTION</span></span>
<span data-ttu-id="11694-106">Il cmdlet **Get-AzCognitiveServicesAccountKey** ottiene le chiavi API per un account di Servizi cognitivi di cui è stato eseguito il provisioning.</span><span class="sxs-lookup"><span data-stu-id="11694-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="11694-107">Un account di Servizi cognitivi ha due chiavi API: Key1 e Key2.</span><span class="sxs-lookup"><span data-stu-id="11694-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="11694-108">Le chiavi consentono l'interazione con l'endpoint dell'account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="11694-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="11694-109">Usare New-AzCognitiveServicesAccountKey chiave per rigenerare una chiave.</span><span class="sxs-lookup"><span data-stu-id="11694-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="11694-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11694-110">EXAMPLES</span></span>

### <span data-ttu-id="11694-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="11694-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="11694-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11694-112">PARAMETERS</span></span>

### <span data-ttu-id="11694-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11694-113">-DefaultProfile</span></span>
<span data-ttu-id="11694-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="11694-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11694-115">-Name</span><span class="sxs-lookup"><span data-stu-id="11694-115">-Name</span></span>
<span data-ttu-id="11694-116">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="11694-116">Specifies the name of the account.</span></span>
<span data-ttu-id="11694-117">Questo cmdlet ottiene le chiavi per questo account.</span><span class="sxs-lookup"><span data-stu-id="11694-117">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11694-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11694-118">-ResourceGroupName</span></span>
<span data-ttu-id="11694-119">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="11694-119">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11694-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11694-120">CommonParameters</span></span>
<span data-ttu-id="11694-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11694-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11694-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="11694-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11694-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="11694-123">INPUTS</span></span>

### <span data-ttu-id="11694-124">System.String</span><span class="sxs-lookup"><span data-stu-id="11694-124">System.String</span></span>

## <span data-ttu-id="11694-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11694-125">OUTPUTS</span></span>

### <span data-ttu-id="11694-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="11694-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="11694-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="11694-127">NOTES</span></span>

## <span data-ttu-id="11694-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11694-128">RELATED LINKS</span></span>

[<span data-ttu-id="11694-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="11694-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


