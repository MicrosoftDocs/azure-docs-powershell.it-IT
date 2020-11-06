---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 247b0735e41f02a55b94e5a8f8ed44136eb3f37e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510359"
---
# <span data-ttu-id="6091f-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6091f-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="6091f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6091f-102">SYNOPSIS</span></span>
<span data-ttu-id="6091f-103">Recupera un elenco di credenziali associate a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="6091f-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6091f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6091f-104">SYNTAX</span></span>

### <span data-ttu-id="6091f-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6091f-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6091f-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6091f-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6091f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6091f-107">DESCRIPTION</span></span>
<span data-ttu-id="6091f-108">Il cmdlet Get-AzureRmADSpCredential può essere usato per recuperare un elenco di credenziali associate a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="6091f-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="6091f-109">Questo comando consente di recuperare tutte le proprietà delle credenziali, ma non il valore delle credenziali, associate all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="6091f-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="6091f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6091f-110">EXAMPLES</span></span>

### <span data-ttu-id="6091f-111">--------------------------Esempio 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6091f-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="6091f-112">Restituisce un elenco di credenziali associate all'entità servizio con SPN ' http://test12345 '.</span><span class="sxs-lookup"><span data-stu-id="6091f-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="6091f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6091f-113">PARAMETERS</span></span>

### <span data-ttu-id="6091f-114">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6091f-114">-ObjectId</span></span>
<span data-ttu-id="6091f-115">ID oggetto dell'entità servizio per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="6091f-115">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6091f-116">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="6091f-116">-ServicePrincipalName</span></span>
<span data-ttu-id="6091f-117">Nome (SPN) dell'entità servizio per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="6091f-117">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6091f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6091f-118">-DefaultProfile</span></span>
<span data-ttu-id="6091f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6091f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6091f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6091f-120">CommonParameters</span></span>
<span data-ttu-id="6091f-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6091f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6091f-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6091f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6091f-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6091f-123">INPUTS</span></span>

## <span data-ttu-id="6091f-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6091f-124">OUTPUTS</span></span>

### <span data-ttu-id="6091f-125">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="6091f-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="6091f-126">Note</span><span class="sxs-lookup"><span data-stu-id="6091f-126">NOTES</span></span>

## <span data-ttu-id="6091f-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6091f-127">RELATED LINKS</span></span>

[<span data-ttu-id="6091f-128">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6091f-128">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="6091f-129">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6091f-129">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="6091f-130">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6091f-130">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

