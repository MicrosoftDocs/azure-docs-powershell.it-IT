---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 806fb4892e0fa68b8e49fe29ec0897abf9be2dc8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488044"
---
# <span data-ttu-id="dcee3-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dcee3-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="dcee3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dcee3-102">SYNOPSIS</span></span>
<span data-ttu-id="dcee3-103">Accedere a un registro di sistema di Azure container.</span><span class="sxs-lookup"><span data-stu-id="dcee3-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="dcee3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dcee3-104">SYNTAX</span></span>

### <span data-ttu-id="dcee3-105">WithoutNameAndPasswordParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dcee3-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcee3-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcee3-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcee3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dcee3-107">DESCRIPTION</span></span>
<span data-ttu-id="dcee3-108">Accedere a un registro di sistema di Azure container.</span><span class="sxs-lookup"><span data-stu-id="dcee3-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="dcee3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dcee3-109">EXAMPLES</span></span>

### <span data-ttu-id="dcee3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dcee3-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="dcee3-111">Accedere a ACR senza credenziali quando si accede già all'account Azure.</span><span class="sxs-lookup"><span data-stu-id="dcee3-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="dcee3-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="dcee3-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="dcee3-113">Accedere a ACR con il nome utente e la password di amministratore quando l'utente ha abilitato l'amministratore.</span><span class="sxs-lookup"><span data-stu-id="dcee3-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="dcee3-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="dcee3-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="dcee3-115">Accedere a ACR con l'ID applicazione e la password di Service Principal.</span><span class="sxs-lookup"><span data-stu-id="dcee3-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="dcee3-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dcee3-116">PARAMETERS</span></span>

### <span data-ttu-id="dcee3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcee3-117">-DefaultProfile</span></span>
<span data-ttu-id="dcee3-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dcee3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcee3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="dcee3-119">-Name</span></span>
<span data-ttu-id="dcee3-120">Nome del registro di sistema di Azure container.</span><span class="sxs-lookup"><span data-stu-id="dcee3-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcee3-121">-Password</span><span class="sxs-lookup"><span data-stu-id="dcee3-121">-Password</span></span>
<span data-ttu-id="dcee3-122">Password per il registro dei contenitori di Azure.</span><span class="sxs-lookup"><span data-stu-id="dcee3-122">Password For Azure Container Registry.</span></span>

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

### <span data-ttu-id="dcee3-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="dcee3-123">-UserName</span></span>
<span data-ttu-id="dcee3-124">Nome utente per il registro dei contenitori di Azure.</span><span class="sxs-lookup"><span data-stu-id="dcee3-124">User Name For Azure Container Registry.</span></span>

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

### <span data-ttu-id="dcee3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcee3-125">CommonParameters</span></span>
<span data-ttu-id="dcee3-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcee3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcee3-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcee3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcee3-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dcee3-128">INPUTS</span></span>

### <span data-ttu-id="dcee3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="dcee3-129">System.String</span></span>

## <span data-ttu-id="dcee3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dcee3-130">OUTPUTS</span></span>

### <span data-ttu-id="dcee3-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dcee3-131">System.Boolean</span></span>

## <span data-ttu-id="dcee3-132">Note</span><span class="sxs-lookup"><span data-stu-id="dcee3-132">NOTES</span></span>

## <span data-ttu-id="dcee3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dcee3-133">RELATED LINKS</span></span>
