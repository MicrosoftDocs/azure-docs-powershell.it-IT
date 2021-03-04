---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: be045303db770cbba919d27ed9563aa64283572c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004461"
---
# <span data-ttu-id="31d41-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="31d41-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="31d41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31d41-102">SYNOPSIS</span></span>
<span data-ttu-id="31d41-103">Accedere a un Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="31d41-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="31d41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31d41-104">SYNTAX</span></span>

### <span data-ttu-id="31d41-105">WithoutNameAndPasswordParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31d41-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31d41-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="31d41-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31d41-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="31d41-107">DESCRIPTION</span></span>
<span data-ttu-id="31d41-108">Accedere a un Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="31d41-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="31d41-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31d41-109">EXAMPLES</span></span>

### <span data-ttu-id="31d41-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="31d41-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="31d41-111">Accedere ad ACR senza credenziali se si esegue già l'accesso all'account azure.</span><span class="sxs-lookup"><span data-stu-id="31d41-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="31d41-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="31d41-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="31d41-113">Accedere ad ACR con nome utente/password di amministratore quando è stato abilitato l'utente amministratore.</span><span class="sxs-lookup"><span data-stu-id="31d41-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="31d41-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="31d41-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="31d41-115">Accedere ad ACR con l'ID applicazione dell'entità servizio e la password.</span><span class="sxs-lookup"><span data-stu-id="31d41-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="31d41-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31d41-116">PARAMETERS</span></span>

### <span data-ttu-id="31d41-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31d41-117">-DefaultProfile</span></span>
<span data-ttu-id="31d41-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31d41-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31d41-119">-Name</span><span class="sxs-lookup"><span data-stu-id="31d41-119">-Name</span></span>
<span data-ttu-id="31d41-120">Nome del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="31d41-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31d41-121">-Password</span><span class="sxs-lookup"><span data-stu-id="31d41-121">-Password</span></span>
<span data-ttu-id="31d41-122">Password per il Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="31d41-122">Password For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d41-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="31d41-123">-UserName</span></span>
<span data-ttu-id="31d41-124">Nome utente per il Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="31d41-124">User Name For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d41-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d41-125">CommonParameters</span></span>
<span data-ttu-id="31d41-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31d41-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d41-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31d41-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d41-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="31d41-128">INPUTS</span></span>

### <span data-ttu-id="31d41-129">System.String</span><span class="sxs-lookup"><span data-stu-id="31d41-129">System.String</span></span>

## <span data-ttu-id="31d41-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31d41-130">OUTPUTS</span></span>

### <span data-ttu-id="31d41-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="31d41-131">System.Boolean</span></span>

## <span data-ttu-id="31d41-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="31d41-132">NOTES</span></span>

## <span data-ttu-id="31d41-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31d41-133">RELATED LINKS</span></span>
