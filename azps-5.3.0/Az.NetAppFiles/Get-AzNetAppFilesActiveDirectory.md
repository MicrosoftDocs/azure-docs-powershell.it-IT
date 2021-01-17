---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 6c082d2e61f81c4e0b8cf9bebefd623584fac3e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474024"
---
# <span data-ttu-id="8e591-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="8e591-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="8e591-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e591-102">SYNOPSIS</span></span>
<span data-ttu-id="8e591-103">Ottiene i dettagli di una configurazione di Active Directory per file di Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="8e591-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="8e591-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e591-104">SYNTAX</span></span>

### <span data-ttu-id="8e591-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8e591-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e591-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e591-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e591-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e591-107">DESCRIPTION</span></span>
<span data-ttu-id="8e591-108">Il cmdlet **Get-AzNetAppFilesActiveDirectory** ottiene i dettagli di una configurazione di Active Directory per gli account ANF.</span><span class="sxs-lookup"><span data-stu-id="8e591-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="8e591-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e591-109">EXAMPLES</span></span>

### <span data-ttu-id="8e591-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8e591-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="8e591-111">Questo comando consente di ottenere la configurazione degli annunci denominata MyADConfigName per l'account ANF (Azure NetApp files) denominato MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="8e591-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="8e591-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e591-112">PARAMETERS</span></span>

### <span data-ttu-id="8e591-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e591-113">-AccountName</span></span>
<span data-ttu-id="8e591-114">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="8e591-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="8e591-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="8e591-115">-AccountObject</span></span>
<span data-ttu-id="8e591-116">Account per il nuovo oggetto Active Directory</span><span class="sxs-lookup"><span data-stu-id="8e591-116">The Account for the new Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e591-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="8e591-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="8e591-118">ActiveDirectoryId di ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="8e591-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActiveDirectoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e591-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e591-119">-DefaultProfile</span></span>
<span data-ttu-id="8e591-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e591-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e591-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e591-121">-ResourceGroupName</span></span>
<span data-ttu-id="8e591-122">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="8e591-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8e591-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e591-123">CommonParameters</span></span>
<span data-ttu-id="8e591-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e591-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e591-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e591-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e591-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e591-126">INPUTS</span></span>

### <span data-ttu-id="8e591-127">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8e591-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="8e591-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e591-128">OUTPUTS</span></span>

### <span data-ttu-id="8e591-129">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="8e591-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="8e591-130">Note</span><span class="sxs-lookup"><span data-stu-id="8e591-130">NOTES</span></span>

## <span data-ttu-id="8e591-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e591-131">RELATED LINKS</span></span>
