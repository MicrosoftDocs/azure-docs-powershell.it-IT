---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: c22643c4ce47fc59d2640a6dbbdf9c15b0846f98
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178855"
---
# <span data-ttu-id="99064-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="99064-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="99064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99064-102">SYNOPSIS</span></span>
<span data-ttu-id="99064-103">Recupera un elenco di credenziali associate a un'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="99064-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="99064-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99064-104">SYNTAX</span></span>

### <span data-ttu-id="99064-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99064-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99064-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="99064-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99064-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="99064-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99064-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99064-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99064-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="99064-109">DESCRIPTION</span></span>
<span data-ttu-id="99064-110">Il Get-AzADSpCredential cmdlet può essere usato per recuperare un elenco di credenziali associate a un'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="99064-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="99064-111">Questo comando recupera tutte le proprietà delle credenziali (ma non il valore delle credenziali) associate all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="99064-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="99064-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99064-112">EXAMPLES</span></span>

### <span data-ttu-id="99064-113">Esempio 1 - Elencare le credenziali per SPN</span><span class="sxs-lookup"><span data-stu-id="99064-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="99064-114">Restituisce un elenco di credenziali associate all'entità servizio con SPN ' http://test12345 '.</span><span class="sxs-lookup"><span data-stu-id="99064-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="99064-115">Esempio 2 - Elencare le credenziali in base all'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="99064-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="99064-116">Restituisce un elenco di credenziali associate all'entità servizio con ID oggetto "58e28616-99cc-4da4-b705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="99064-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="99064-117">Esempio 3 - Elencare le credenziali tramite piping</span><span class="sxs-lookup"><span data-stu-id="99064-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="99064-118">Ottiene l'entità servizio con ID oggetto "58e28616-99cc-4da4-b705-7672130e1047" e la pipe al cmdlet di Get-AzADSpCredential per elencare tutte le credenziali per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="99064-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="99064-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99064-119">PARAMETERS</span></span>

### <span data-ttu-id="99064-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99064-120">-DefaultProfile</span></span>
<span data-ttu-id="99064-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="99064-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99064-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="99064-122">-DisplayName</span></span>
<span data-ttu-id="99064-123">Nome visualizzato dell'entità servizio</span><span class="sxs-lookup"><span data-stu-id="99064-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="99064-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="99064-124">-ObjectId</span></span>
<span data-ttu-id="99064-125">ID oggetto dell'entità servizio da cui recuperare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="99064-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99064-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="99064-126">-ServicePrincipalName</span></span>
<span data-ttu-id="99064-127">Nome (SPN) dell'entità servizio da cui recuperare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="99064-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="99064-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="99064-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="99064-129">Oggetto entità servizio da cui recuperare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="99064-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99064-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99064-130">CommonParameters</span></span>
<span data-ttu-id="99064-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99064-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99064-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="99064-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99064-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="99064-133">INPUTS</span></span>

### <span data-ttu-id="99064-134">System.String</span><span class="sxs-lookup"><span data-stu-id="99064-134">System.String</span></span>

### <span data-ttu-id="99064-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="99064-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="99064-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99064-136">OUTPUTS</span></span>

### <span data-ttu-id="99064-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="99064-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="99064-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="99064-138">NOTES</span></span>

## <span data-ttu-id="99064-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99064-139">RELATED LINKS</span></span>

[<span data-ttu-id="99064-140">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="99064-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="99064-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="99064-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="99064-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="99064-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

