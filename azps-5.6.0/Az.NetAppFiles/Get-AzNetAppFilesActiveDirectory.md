---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7198e34e7e888c2e89fce6cb5293bfc46bf57b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968638"
---
# <span data-ttu-id="d78b3-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d78b3-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="d78b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d78b3-102">SYNOPSIS</span></span>
<span data-ttu-id="d78b3-103">Recupera i dettagli di una configurazione di Azure NetApp Files (ANF) Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d78b3-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="d78b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d78b3-104">SYNTAX</span></span>

### <span data-ttu-id="d78b3-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d78b3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d78b3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d78b3-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d78b3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d78b3-107">DESCRIPTION</span></span>
<span data-ttu-id="d78b3-108">Il **cmdlet Get-AzNetAppFilesActiveDirectory** ottiene i dettagli di una configurazione di Active Directory degli account ANF.</span><span class="sxs-lookup"><span data-stu-id="d78b3-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="d78b3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d78b3-109">EXAMPLES</span></span>

### <span data-ttu-id="d78b3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d78b3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="d78b3-111">Questo comando recupera la configurazione di Active Directory denominata MyADConfigName per l'account Azure NetApp Files (ANF) denominato MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="d78b3-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="d78b3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d78b3-112">PARAMETERS</span></span>

### <span data-ttu-id="d78b3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d78b3-113">-AccountName</span></span>
<span data-ttu-id="d78b3-114">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="d78b3-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="d78b3-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="d78b3-115">-AccountObject</span></span>
<span data-ttu-id="d78b3-116">Account per il nuovo oggetto Active Directory</span><span class="sxs-lookup"><span data-stu-id="d78b3-116">The Account for the new Active Directory object</span></span>

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

### <span data-ttu-id="d78b3-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="d78b3-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="d78b3-118">ActiveDirectoryId di ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="d78b3-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

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

### <span data-ttu-id="d78b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d78b3-119">-DefaultProfile</span></span>
<span data-ttu-id="d78b3-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d78b3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d78b3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d78b3-121">-ResourceGroupName</span></span>
<span data-ttu-id="d78b3-122">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="d78b3-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d78b3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d78b3-123">CommonParameters</span></span>
<span data-ttu-id="d78b3-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d78b3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d78b3-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d78b3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d78b3-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="d78b3-126">INPUTS</span></span>

### <span data-ttu-id="d78b3-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d78b3-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d78b3-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d78b3-128">OUTPUTS</span></span>

### <span data-ttu-id="d78b3-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d78b3-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="d78b3-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="d78b3-130">NOTES</span></span>

## <span data-ttu-id="d78b3-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d78b3-131">RELATED LINKS</span></span>
