---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: 4969ba5cdb8b24627e620b82a13806c7b4cc687e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187447"
---
# <span data-ttu-id="67e3a-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="67e3a-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="67e3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="67e3a-103">Ottiene le chiavi API per un account.</span><span class="sxs-lookup"><span data-stu-id="67e3a-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="67e3a-104">Queste chiavi sono il meccanismo di autenticazione utilizzato nelle chiamate successive ad Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="67e3a-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="67e3a-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67e3a-105">SYNTAX</span></span>

### <span data-ttu-id="67e3a-106">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="67e3a-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67e3a-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67e3a-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67e3a-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67e3a-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67e3a-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67e3a-109">DESCRIPTION</span></span>
<span data-ttu-id="67e3a-110">Il cmdlet Get-AzMapsAccountKey cmdlet ottiene le chiavi API per un account di Azure Maps di cui è stato eseguito il provisioning.</span><span class="sxs-lookup"><span data-stu-id="67e3a-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="67e3a-111">Un account di Mappe di Azure ha due chiavi API: primaria e secondaria.</span><span class="sxs-lookup"><span data-stu-id="67e3a-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="67e3a-112">Le chiavi consentono l'interazione con l'endpoint dell'account di Mappe di Azure.</span><span class="sxs-lookup"><span data-stu-id="67e3a-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="67e3a-113">Usare New-AzMapsAccountKey (New-AzMapsAccountKey.md)per rigenerare una chiave.</span><span class="sxs-lookup"><span data-stu-id="67e3a-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="67e3a-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67e3a-114">EXAMPLES</span></span>

### <span data-ttu-id="67e3a-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="67e3a-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="67e3a-116">Restituisce le chiavi dell'account denominato MyAccount nel gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="67e3a-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="67e3a-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="67e3a-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="67e3a-118">Restituisce le chiavi per l'account di Azure Maps specificato.</span><span class="sxs-lookup"><span data-stu-id="67e3a-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="67e3a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67e3a-119">PARAMETERS</span></span>

### <span data-ttu-id="67e3a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e3a-120">-DefaultProfile</span></span>
<span data-ttu-id="67e3a-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67e3a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67e3a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67e3a-122">-InputObject</span></span>
<span data-ttu-id="67e3a-123">Mappe dell'account in pipe da Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="67e3a-123">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67e3a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="67e3a-124">-Name</span></span>
<span data-ttu-id="67e3a-125">Nome account mappe.</span><span class="sxs-lookup"><span data-stu-id="67e3a-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e3a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67e3a-126">-ResourceGroupName</span></span>
<span data-ttu-id="67e3a-127">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="67e3a-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e3a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67e3a-128">-ResourceId</span></span>
<span data-ttu-id="67e3a-129">Mappe Id ResourceId account.</span><span class="sxs-lookup"><span data-stu-id="67e3a-129">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e3a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e3a-130">CommonParameters</span></span>
<span data-ttu-id="67e3a-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67e3a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e3a-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e3a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e3a-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="67e3a-133">INPUTS</span></span>

### <span data-ttu-id="67e3a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="67e3a-134">System.String</span></span>

### <span data-ttu-id="67e3a-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="67e3a-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="67e3a-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67e3a-136">OUTPUTS</span></span>

### <span data-ttu-id="67e3a-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="67e3a-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="67e3a-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="67e3a-138">NOTES</span></span>

## <span data-ttu-id="67e3a-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67e3a-139">RELATED LINKS</span></span>
