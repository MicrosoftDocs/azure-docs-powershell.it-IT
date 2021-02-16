---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194094"
---
# <span data-ttu-id="a35ba-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="a35ba-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="a35ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a35ba-102">SYNOPSIS</span></span>
<span data-ttu-id="a35ba-103">Ottenere le chiavi dell'account di rendering remoto</span><span class="sxs-lookup"><span data-stu-id="a35ba-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="a35ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a35ba-104">SYNTAX</span></span>

### <span data-ttu-id="a35ba-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="a35ba-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a35ba-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a35ba-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a35ba-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="a35ba-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a35ba-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a35ba-108">DESCRIPTION</span></span>
<span data-ttu-id="a35ba-109">Ottieni le chiavi per sviluppatori di Remote Rendering Account.</span><span class="sxs-lookup"><span data-stu-id="a35ba-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="a35ba-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a35ba-110">EXAMPLES</span></span>

### <span data-ttu-id="a35ba-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a35ba-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="a35ba-112">Ottenere le chiavi per sviluppatori di Remote Rendering Account "example" dalla sottoscrizione corrente e dal gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="a35ba-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="a35ba-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a35ba-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="a35ba-114">Ottenere le chiavi per sviluppatori di Remote Rendering Account "example" dalla sottoscrizione corrente e dal gruppo di risorse "rg1" con piping.</span><span class="sxs-lookup"><span data-stu-id="a35ba-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="a35ba-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a35ba-115">PARAMETERS</span></span>

### <span data-ttu-id="a35ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a35ba-116">-DefaultProfile</span></span>
<span data-ttu-id="a35ba-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a35ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a35ba-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a35ba-118">-InputObject</span></span>
<span data-ttu-id="a35ba-119">L'oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a35ba-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a35ba-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a35ba-120">-Name</span></span>
<span data-ttu-id="a35ba-121">Nome dell'account per il rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="a35ba-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a35ba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a35ba-122">-ResourceGroupName</span></span>
<span data-ttu-id="a35ba-123">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a35ba-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a35ba-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a35ba-124">-ResourceId</span></span>
<span data-ttu-id="a35ba-125">ID risorsa dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="a35ba-125">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a35ba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35ba-126">CommonParameters</span></span>
<span data-ttu-id="a35ba-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a35ba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a35ba-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a35ba-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35ba-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="a35ba-129">INPUTS</span></span>

### <span data-ttu-id="a35ba-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a35ba-130">System.String</span></span>

### <span data-ttu-id="a35ba-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="a35ba-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="a35ba-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a35ba-132">OUTPUTS</span></span>

### <span data-ttu-id="a35ba-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a35ba-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="a35ba-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="a35ba-134">NOTES</span></span>

## <span data-ttu-id="a35ba-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a35ba-135">RELATED LINKS</span></span>
