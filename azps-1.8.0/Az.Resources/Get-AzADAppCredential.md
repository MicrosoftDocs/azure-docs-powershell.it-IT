---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: fdef07255316b1d7529202c36b844e8732c76390
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677422"
---
# <span data-ttu-id="6981b-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="6981b-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="6981b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6981b-102">SYNOPSIS</span></span>
<span data-ttu-id="6981b-103">Recupera un elenco di credenziali associate a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6981b-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="6981b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6981b-104">SYNTAX</span></span>

### <span data-ttu-id="6981b-105">ApplicationObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6981b-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6981b-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6981b-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6981b-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6981b-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6981b-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6981b-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6981b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6981b-109">DESCRIPTION</span></span>
<span data-ttu-id="6981b-110">Il cmdlet Get-AzADAppCredential può essere usato per recuperare un elenco di credenziali associate a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6981b-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="6981b-111">Questo comando consente di recuperare tutte le proprietà delle credenziali, ma non il valore delle credenziali, associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6981b-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="6981b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6981b-112">EXAMPLES</span></span>

### <span data-ttu-id="6981b-113">Esempio 1-ottenere le credenziali dell'applicazione per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="6981b-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="6981b-114">Restituisce un elenco di credenziali associate all'applicazione con l'ID oggetto "1f99cf81-0146-4f4e-BEAE-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="6981b-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="6981b-115">Esempio 2-ottenere le credenziali dell'applicazione tramite pipe</span><span class="sxs-lookup"><span data-stu-id="6981b-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="6981b-116">Ottiene l'applicazione con l'ID oggetto "1f99cf81-0146-4f4e-BEAE-2007d0668476" e la convoglia al cmdlet Get-AzADAppCredential per elencare tutte le credenziali per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6981b-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="6981b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6981b-117">PARAMETERS</span></span>

### <span data-ttu-id="6981b-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6981b-118">-ApplicationId</span></span>
<span data-ttu-id="6981b-119">ID dell'applicazione per cui recuperare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="6981b-119">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6981b-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="6981b-120">-ApplicationObject</span></span>
<span data-ttu-id="6981b-121">L'oggetto Application per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="6981b-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6981b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6981b-122">-DefaultProfile</span></span>
<span data-ttu-id="6981b-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6981b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6981b-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6981b-124">-DisplayName</span></span>
<span data-ttu-id="6981b-125">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6981b-125">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6981b-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6981b-126">-ObjectId</span></span>
<span data-ttu-id="6981b-127">ID oggetto dell'applicazione per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="6981b-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="6981b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6981b-128">CommonParameters</span></span>
<span data-ttu-id="6981b-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6981b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6981b-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6981b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6981b-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6981b-131">INPUTS</span></span>

### <span data-ttu-id="6981b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6981b-132">System.String</span></span>

### <span data-ttu-id="6981b-133">System. Guid</span><span class="sxs-lookup"><span data-stu-id="6981b-133">System.Guid</span></span>

### <span data-ttu-id="6981b-134">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="6981b-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="6981b-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6981b-135">OUTPUTS</span></span>

### <span data-ttu-id="6981b-136">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="6981b-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="6981b-137">Note</span><span class="sxs-lookup"><span data-stu-id="6981b-137">NOTES</span></span>

## <span data-ttu-id="6981b-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6981b-138">RELATED LINKS</span></span>

[<span data-ttu-id="6981b-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="6981b-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="6981b-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="6981b-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="6981b-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6981b-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
