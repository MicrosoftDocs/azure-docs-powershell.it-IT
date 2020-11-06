---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: e270a59e3799302eed49a0fd60180bb8d4589d92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521546"
---
# <span data-ttu-id="67214-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="67214-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="67214-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67214-102">SYNOPSIS</span></span>
<span data-ttu-id="67214-103">Recupera un elenco di credenziali associate a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="67214-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67214-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67214-104">SYNTAX</span></span>

### <span data-ttu-id="67214-105">ApplicationObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67214-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67214-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67214-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67214-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67214-107">DESCRIPTION</span></span>
<span data-ttu-id="67214-108">Il cmdlet Get-AzureRmADAppCredential può essere usato per recuperare un elenco di credenziali associate a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="67214-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="67214-109">Questo comando consente di recuperare tutte le proprietà delle credenziali, ma non il valore delle credenziali, associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="67214-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="67214-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67214-110">EXAMPLES</span></span>

### <span data-ttu-id="67214-111">--------------------------Esempio 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="67214-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="67214-112">Restituisce un elenco di credenziali associate all'applicazione con l'ID oggetto "1f99cf81-0146-4f4e-BEAE-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="67214-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="67214-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67214-113">PARAMETERS</span></span>

### <span data-ttu-id="67214-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="67214-114">-ApplicationId</span></span>
<span data-ttu-id="67214-115">ID dell'applicazione per cui recuperare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="67214-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67214-116">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="67214-116">-ObjectId</span></span>
<span data-ttu-id="67214-117">ID oggetto dell'applicazione per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="67214-117">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67214-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67214-118">-DefaultProfile</span></span>
<span data-ttu-id="67214-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67214-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67214-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67214-120">CommonParameters</span></span>
<span data-ttu-id="67214-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67214-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67214-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67214-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67214-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67214-123">INPUTS</span></span>

## <span data-ttu-id="67214-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67214-124">OUTPUTS</span></span>

### <span data-ttu-id="67214-125">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="67214-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="67214-126">Note</span><span class="sxs-lookup"><span data-stu-id="67214-126">NOTES</span></span>

## <span data-ttu-id="67214-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67214-127">RELATED LINKS</span></span>

[<span data-ttu-id="67214-128">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="67214-128">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="67214-129">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="67214-129">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="67214-130">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="67214-130">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

